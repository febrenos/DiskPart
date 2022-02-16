# DiskPart cmd
Partitions manager, clean disk, format

#### FORMAT
--------------------------------------------------------
- diskpart
- list disk
- select disk 1
- clean
- create partition primary
- select partition 1
- active
- format fs=ntfs quick
- assign
- exit

#### FORMAT
--------------------------------------------------------
- diskpart
- list disk
- select disk 1
- clean
- create partition primary
- format fs=fat || format fs=ntfs
- assign || assign letter=f

#### CONVERT GPT || MBR
--------------------------------------------------------
- diskpart
- list disk
- select disk 1
- clean
- convert gpt || convert mbr 

#### CREATE PARTITION
--------------------------------------------------------
- diskpart
- list disk
- select disk 1
- list vol
- select vol 1
- shrink desired=2048 (2GB)
- create partition extended size=2048
- select partition 1
- create partition logical
- format fs=ntfs || format fs=ntfs quick label=”Tutorial”

#### DELETE PARTITION
--------------------------------------------------------
- select partition 1
- delete partition override

#### ON || OFF
--------------------------------------------------------
- offline disk
- online disk

#### MORE INFORMATION
--------------------------------------------------------
- help
