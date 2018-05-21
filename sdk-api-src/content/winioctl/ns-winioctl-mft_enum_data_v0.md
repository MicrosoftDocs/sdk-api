---
UID: NS:winioctl.MFT_ENUM_DATA_V0
title: MFT_ENUM_DATA_V0
author: windows-driver-content
description: Contains information defining the boundaries for and starting place of an enumeration of update sequence number (USN) change journal records.
old-location: fs\mft_enum_data_str.htm
old-project: FileIO
ms.assetid: bd098d10-b30f-44b0-a379-2d57e33fe1c9
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PMFT_ENUM_DATA, *PMFT_ENUM_DATA_V0, MFT_ENUM_DATA, MFT_ENUM_DATA_V0, MFT_ENUM_DATA_V0 structure [Files], PMFT_ENUM_DATA_V0, PMFT_ENUM_DATA_V0 structure pointer [Files], _win32_mft_enum_data_str, base.mft_enum_data_str, fs.mft_enum_data_str, winioctl/MFT_ENUM_DATA_V0, winioctl/PMFT_ENUM_DATA_V0"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFT_ENUM_DATA_V0, *PMFT_ENUM_DATA_V0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	MFT_ENUM_DATA_V0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

