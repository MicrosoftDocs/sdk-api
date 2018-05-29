---
UID: NS:winioctl._GET_LENGTH_INFORMATION
title: "_GET_LENGTH_INFORMATION"
author: windows-sdk-content
description: Contains disk, volume, or partition length information used by the IOCTL_DISK_GET_LENGTH_INFO control code.
old-location: fs\get_length_information_str.htm
old-project: FileIO
ms.assetid: a0d2a5bc-32e0-47d6-a4f0-84bd7f6bb746
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PGET_LENGTH_INFORMATION, GET_LENGTH_INFORMATION, GET_LENGTH_INFORMATION structure [Files], _GET_LENGTH_INFORMATION, _win32_get_length_information_str, base.get_length_information_str, fs.get_length_information_str, winioctl/GET_LENGTH_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GET_LENGTH_INFORMATION, *PGET_LENGTH_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	GET_LENGTH_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _GET_LENGTH_INFORMATION structure


## -description


Contains disk, volume, or partition length information used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560370">IOCTL_DISK_GET_LENGTH_INFO</a> control code.


## -struct-fields




### -field Length

The length of the disk, volume, or partition, in bytes.
					


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560370">IOCTL_DISK_GET_LENGTH_INFO</a>
 

 

