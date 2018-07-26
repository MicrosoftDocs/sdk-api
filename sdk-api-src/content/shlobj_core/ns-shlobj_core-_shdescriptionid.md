---
UID: NS:shlobj_core._SHDESCRIPTIONID
title: "_SHDESCRIPTIONID"
author: windows-sdk-content
description: Receives item data in response to a call to SHGetDataFromIDList.
old-location: shell\SHDESCRIPTIONID_str.htm
old-project: shell
ms.assetid: dca32567-2049-4797-af87-d08a5d5d055d
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: "*LPSHDESCRIPTIONID, LPSHDESCRIPTIONID, LPSHDESCRIPTIONID structure pointer [Windows Shell], SHDESCRIPTIONID, SHDESCRIPTIONID structure [Windows Shell], SHDID_COMPUTER_AUDIO, SHDID_COMPUTER_CDROM, SHDID_COMPUTER_DRIVE35, SHDID_COMPUTER_DRIVE525, SHDID_COMPUTER_FIXED, SHDID_COMPUTER_IMAGING, SHDID_COMPUTER_NETDRIVE, SHDID_COMPUTER_OTHER, SHDID_COMPUTER_RAMDISK, SHDID_COMPUTER_REMOVABLE, SHDID_COMPUTER_SHAREDDOCS, SHDID_FS_DIRECTORY, SHDID_FS_FILE, SHDID_FS_OTHER, SHDID_MOBILE_DEVICE, SHDID_NET_DOMAIN, SHDID_NET_OTHER, SHDID_NET_RESTOFNET, SHDID_NET_SERVER, SHDID_NET_SHARE, SHDID_ROOT_REGITEM, _SHDESCRIPTIONID, _win32_SHDESCRIPTIONID_str, shell.SHDESCRIPTIONID_str, shlobj_core/LPSHDESCRIPTIONID, shlobj_core/SHDESCRIPTIONID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHDESCRIPTIONID, *LPSHDESCRIPTIONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHDESCRIPTIONID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
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

