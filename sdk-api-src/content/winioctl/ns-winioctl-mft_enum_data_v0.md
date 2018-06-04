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

# MFT_ENUM_DATA_V0 structure


## -description


Contains information defining the boundaries for and starting place of an enumeration of update 
    sequence number (USN) change journal records. It is used as the input buffer for the 
    <a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a> control code. Prior to 
    Windows Server 2012 this structure was named 
    <b>MFT_ENUM_DATA</b>. Use that name to compile with older SDKs 
    and compilers.


## -struct-fields




### -field StartFileReferenceNumber

The ordinal position within the files on the current volume at which the enumeration is to begin.

The first call to <a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a> during an 
       enumeration must have the <b>StartFileReferenceNumber</b> member set to 
       <code>(DWORDLONG)0</code>. Each call to 
       <b>FSCTL_ENUM_USN_DATA</b> retrieves the starting point for 
       the subsequent call as the first entry in the output buffer. Subsequent calls must be made with 
       <b>StartFileReferenceNumber</b> set to this value. For more information, see 
       <b>FSCTL_ENUM_USN_DATA</b>.


### -field LowUsn

The lower boundary of the range of USN values used to filter which records are returned. Only records whose 
      last change journal USN is between or equal to the <b>LowUsn</b> and 
      <b>HighUsn</b> member values are returned.


### -field HighUsn

The upper boundary of the range of USN values used to filter which files are returned.


## -see-also




<a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

