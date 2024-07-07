# Let's Encrypt / certbot notes

## HAProxy - auto renew

Note: This approach will result with a short HAProxy downtime.

Create a pre/post renewal hook as in the [pre](pre)/[post](post) directories.

Note: don't forget to replace the `example.com` domain with your own.

Make the files executable

```bash
#!/bin/bash

sudo chmod +x /etc/letsencrypt/renewal-hooks/pre/haproxy.sh
sudo chmod +x /etc/letsencrypt/renewal-hooks/post/haproxy.sh
```

Dry run:

`sudo certbot renew --dry-run`

## Contributing

Feel free to create a PR to improve the existing hooks or provide pre/post hooks
for other systems/scenarios.

## References

- [certbot](https://certbot.eff.org/)
