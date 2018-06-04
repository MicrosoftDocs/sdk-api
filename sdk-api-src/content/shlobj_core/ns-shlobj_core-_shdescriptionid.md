---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SHDESCRIPTIONID structure


## -description


Receives item data in response to a call to <a href="https://msdn.microsoft.com/11c041bd-22fd-46a4-b75c-cc86ee771241">SHGetDataFromIDList</a>.


## -struct-fields




### -field dwDescriptionId

Type: <b>DWORD</b>

Receives a value that determines what type the item is. One of the following values.



#### SHDID_ROOT_REGITEM

The item is a registered item on the desktop.



#### SHDID_FS_FILE

The item is a file.



#### SHDID_FS_DIRECTORY

The item is a folder.



#### SHDID_FS_OTHER

The item is an unidentified item in the file system.



#### SHDID_COMPUTER_DRIVE35

The item is a 3.5-inch floppy drive.



#### SHDID_COMPUTER_DRIVE525

The item is a 5.25-inch floppy drive.



#### SHDID_COMPUTER_REMOVABLE

The item is a removable disk.



#### SHDID_COMPUTER_FIXED

The item is a fixed hard disk.



#### SHDID_COMPUTER_NETDRIVE

The item is a drive that is mapped to a network share.



#### SHDID_COMPUTER_CDROM

The item is a CD-ROM drive.



#### SHDID_COMPUTER_RAMDISK

The item is a RAM disk.



#### SHDID_COMPUTER_OTHER

The item is an unidentified system device.



#### SHDID_NET_DOMAIN

The item is a network domain.



#### SHDID_NET_SERVER

The item is a network server.



#### SHDID_NET_SHARE

The item is a network share.



#### SHDID_NET_RESTOFNET

Not currently used.



#### SHDID_NET_OTHER

The item is an unidentified network resource.



#### SHDID_COMPUTER_IMAGING

<b>Windows XP and later</b>. Not currently used.



#### SHDID_COMPUTER_AUDIO

<b>Windows XP and later</b>. Not currently used.



#### SHDID_COMPUTER_SHAREDDOCS

<b>Windows XP and later</b>. The item is the system shared documents folder.



#### SHDID_MOBILE_DEVICE

<b>Windows Vista and later.</b> The item is a mobile device, such as a personal digital assistant (PDA).


### -field clsid

Type: <b>CLSID</b>

Receives the CLSID of the object to which the item belongs.

