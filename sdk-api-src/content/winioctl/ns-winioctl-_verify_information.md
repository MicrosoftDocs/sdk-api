---
UID: NS:winioctl._VERIFY_INFORMATION
title: "_VERIFY_INFORMATION"
author: windows-sdk-content
description: Contains information used to verify a disk extent.
old-location: fs\verify_information_str.htm
old-project: FileIO
ms.assetid: bf987bb5-b3d8-4d5b-af44-d05fbe4c0a5c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PVERIFY_INFORMATION, PVERIFY_INFORMATION, PVERIFY_INFORMATION structure pointer [Files], VERIFY_INFORMATION, VERIFY_INFORMATION structure [Files], _VERIFY_INFORMATION, _win32_verify_information_str, base.verify_information_str, fs.verify_information_str, winioctl/PVERIFY_INFORMATION, winioctl/VERIFY_INFORMATION"
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
tech.root: 
req.typenames: VERIFY_INFORMATION, *PVERIFY_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - VERIFY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _VERIFY_INFORMATION structure


## -description


Contains information used to verify a disk extent. It is the output buffer for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560420">IOCTL_DISK_VERIFY</a> control code.


## -struct-fields




### -field StartingOffset

The starting offset of the disk extent. 


### -field Length

The length of the disk extent, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560420">IOCTL_DISK_VERIFY</a>
 

 

