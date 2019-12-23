## Tổng hợp các mẹo và kiến thức
Đây là repo tổng hợp lại 1 số kinh nghiệm của tôi về quản trị hệ thống.

## Extend the LVM Logical Volume



```bash
# extend the existing volume group to include this new sda3 space (+6GB)
# or run: `lvextend -l +100%FREE` which means use all space available
lvextend -L+6G /dev/ubuntu-vg/root /dev/sda3

# force space recognized
resize2fs /dev/ubuntu-vg/root

# Validate Increased Capacity
df -h
```

* Ubuntu: https://www.evernote.com/shard/s419/sh/1bc2b2fb-dbfc-47ee-8774-eca7c860a876/a05682226781837460c7ad7ff01e2ed0
