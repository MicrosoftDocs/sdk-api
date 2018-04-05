---
UID: NS:winioctl.USN_RANGE_TRACK_OUTPUT
title: USN_RANGE_TRACK_OUTPUT
author: windows-driver-content
description: Contains returned update sequence number (USN) from FSCTL_USN_TRACK_MODIFIED_RANGES control code.
old-location: fs\usn_range_track_output.htm
old-project: FileIO
ms.assetid: E10ECB50-A506-4836-81D2-3073FBB844CA
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PUSN_RANGE_TRACK_OUTPUT, PUSN_RANGE_TRACK_OUTPUT, PUSN_RANGE_TRACK_OUTPUT structure pointer [Files], USN_RANGE_TRACK_OUTPUT, USN_RANGE_TRACK_OUTPUT structure [Files], fs.usn_range_track_output, winioctl/PUSN_RANGE_TRACK_OUTPUT, winioctl/USN_RANGE_TRACK_OUTPUT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USN_RANGE_TRACK_OUTPUT, *PUSN_RANGE_TRACK_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	USN_RANGE_TRACK_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# USN_RANGE_TRACK_OUTPUT structure


## -description


Contains returned update sequence number (USN) from <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.


## -struct-fields




### -field Usn

Returned update sequence number (USN) that identifies at what point in the USN Journal that range tracking was enabled.


## -remarks



This structure is optional.




## -see-also




<a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a>
 

 

