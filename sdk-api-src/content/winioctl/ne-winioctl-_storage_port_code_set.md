---
UID: NE:winioctl._STORAGE_PORT_CODE_SET
title: "_STORAGE_PORT_CODE_SET"
author: windows-sdk-content
description: Reserved for system use.
old-location: fs\storage_port_code_set.htm
tech.root: FileIO
ms.assetid: 1c1032e8-30b8-45ad-973a-c7616139b26e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PSTORAGE_PORT_CODE_SET, PSTORAGE_PORT_CODE_SET, PSTORAGE_PORT_CODE_SET enumeration pointer [Files], STORAGE_PORT_CODE_SET, STORAGE_PORT_CODE_SET enumeration [Files], StoragePortCodeSetATAport, StoragePortCodeSetReserved, StoragePortCodeSetSBP2port, StoragePortCodeSetSCSIport, StoragePortCodeSetSDport, StoragePortCodeSetSpaceport, StoragePortCodeSetStorport, StoragePortCodeSetUSBport, _STORAGE_PORT_CODE_SET, fs.storage_port_code_set, winioctl/PSTORAGE_PORT_CODE_SET, winioctl/STORAGE_PORT_CODE_SET, winioctl/StoragePortCodeSetATAport, winioctl/StoragePortCodeSetReserved, winioctl/StoragePortCodeSetSBP2port, winioctl/StoragePortCodeSetSCSIport, winioctl/StoragePortCodeSetSDport, winioctl/StoragePortCodeSetSpaceport, winioctl/StoragePortCodeSetStorport, winioctl/StoragePortCodeSetUSBport"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PORT_CODE_SET
product: Windows
targetos: Windows
req.typenames: STORAGE_PORT_CODE_SET, *PSTORAGE_PORT_CODE_SET
req.redist: 
---

# _STORAGE_PORT_CODE_SET enumeration


## -description


Reserved for system use. 


## -enum-fields




### -field StoragePortCodeSetReserved

Indicates an unknown storage adapter driver type.


### -field StoragePortCodeSetStorport

Storage adapter driver is a Storport-miniport driver.


### -field StoragePortCodeSetSCSIport

Storage adapter driver is a SCSI Port-miniport driver.


### -field StoragePortCodeSetSpaceport

Storage adapter driver is the Spaceport driver.


### -field StoragePortCodeSetATAport

Storage adapter driver is an ATA-port miniport driver.


### -field StoragePortCodeSetUSBport

Storage adapter driver is the  USB-storage port driver.


### -field StoragePortCodeSetSBP2port

Storage adapter driver is the  SBP2 port driver.


### -field StoragePortCodeSetSDport

Storage adapter driver is an SD-port miniport driver.


## -see-also




<a href="https://msdn.microsoft.com/ed8fe5c1-dbdf-43bc-a0a7-17e541eba950">Disk Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/b962666d-60ae-4e0b-813e-7b22e1670644">STORAGE_MINIPORT_DESCRIPTOR</a>
 

 

