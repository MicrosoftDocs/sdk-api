---
UID: NS:winioctl._PREVENT_MEDIA_REMOVAL
title: "_PREVENT_MEDIA_REMOVAL"
author: windows-sdk-content
description: Provides removable media locking data. It is used by the IOCTL_STORAGE_MEDIA_REMOVAL control code.
old-location: base\prevent_media_removal_str.htm
tech.root: devio
ms.assetid: a5f55555-5226-46a7-8869-df4d1c4e7352
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPREVENT_MEDIA_REMOVAL, PREVENT_MEDIA_REMOVAL, PREVENT_MEDIA_REMOVAL structure, _PREVENT_MEDIA_REMOVAL, _win32_prevent_media_removal_str, base.prevent_media_removal_str, winioctl/PREVENT_MEDIA_REMOVAL"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - PREVENT_MEDIA_REMOVAL
product: Windows
targetos: Windows
req.typenames: PREVENT_MEDIA_REMOVAL, *PPREVENT_MEDIA_REMOVAL
req.redist: 
---

# _PREVENT_MEDIA_REMOVAL structure


## -description


Provides removable media locking data. It is used by the 
<a href="https://msdn.microsoft.com/5971daa1-3bb7-4050-b252-2f5cabb1bf67">IOCTL_STORAGE_MEDIA_REMOVAL</a> control code.


## -struct-fields




### -field PreventMediaRemoval

If this member is <b>TRUE</b>, the media is to be locked. Otherwise, it is not.


## -see-also




<a href="https://msdn.microsoft.com/5971daa1-3bb7-4050-b252-2f5cabb1bf67">IOCTL_STORAGE_MEDIA_REMOVAL</a>
 

 

