FROM stilliard/pure-ftpd:hardened

ENV FTP_MAX_CLIENTS=50

CMD /run.sh \
  -c 100 \
  -C 100 \
  -l puredb:/etc/pure-ftpd/pureftpd.pdb \
  -E \
  -j \
  -R \
  -P $PUBLICHOST \
  -p 30000:30199 \
  -O w3c:/var/log/pure-ftpd/transfer.log \
  --tls=2

EXPOSE 21 30000-30099
