---
UID: NS:ntmsapi._NTMS_ALLOCATION_INFORMATION
title: "_NTMS_ALLOCATION_INFORMATION"
author: windows-sdk-content
description: The NTMS_ALLOCATION_INFORMATION structure contains information about the source media pool from which a medium was taken.
old-location: fs\ntms_allocation_information.htm
old-project: Rsm
ms.assetid: 6861dcea-7f50-4175-85f1-b59478d6c119
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: "*LPNTMS_ALLOCATION_INFORMATION, LPNTMS_ALLOCATION_INFORMATION, LPNTMS_ALLOCATION_INFORMATION structure pointer [Files], NTMS_ALLOCATION_INFORMATION, NTMS_ALLOCATION_INFORMATION structure [Files], _NTMS_ALLOCATION_INFORMATION, _zaw_ntms_allocation_information, base.ntms_allocation_information, fs.ntms_allocation_information, ntmsapi/LPNTMS_ALLOCATION_INFORMATION, ntmsapi/NTMS_ALLOCATION_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntmsapi.h
req.include-header: 
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
req.typenames: NTMS_ALLOCATION_INFORMATION, *LPNTMS_ALLOCATION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_ALLOCATION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _NTMS_ALLOCATION_INFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_ALLOCATION_INFORMATION</b> structure contains information about the source media pool from which a medium was taken.


## -struct-fields




### -field dwSize

Size of the structure.


### -field lpReserved.ptr

 


### -field lpReserved

Reserved.


### -field AllocatedFrom

Unique identifier of the original source of the media.


## -see-also




<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a>
 

 

