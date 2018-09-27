---
UID: NS:winioctl.USN_RECORD_COMMON_HEADER
title: USN_RECORD_COMMON_HEADER
author: windows-sdk-content
description: Contains the information for an update sequence number (USN) common header which is common through USN_RECORD_V2, USN_RECORD_V3 and USN_RECORD_V4.
old-location: fs\usn_record_common_header.htm
tech.root: fileio
ms.assetid: 7B193D8E-FEED-4289-B40F-33BC27889F15
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PUSN_RECORD_COMMON_HEADER, PUSN_RECORD_COMMON_HEADER, PUSN_RECORD_COMMON_HEADER structure pointer [Files], USN_RECORD_COMMON_HEADER, USN_RECORD_COMMON_HEADER structure [Files], fs.usn_record_common_header, winioctl/PUSN_RECORD_COMMON_HEADER, winioctl/USN_RECORD_COMMON_HEADER"
ms.prod: windows
ms.technology: windows-sdk
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
 - USN_RECORD_COMMON_HEADER
product: Windows
targetos: Windows
req.typenames: USN_RECORD_COMMON_HEADER, *PUSN_RECORD_COMMON_HEADER
req.redist: 
---

# USN_RECORD_COMMON_HEADER structure


## -description


Contains the information for an update sequence number (USN) common header which is common through <a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD_V2</a>, <a href="https://msdn.microsoft.com/6d95c5d1-6c6b-498f-a00d-eaa540e8b15b">USN_RECORD_V3</a> and <a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a>.


## -struct-fields




### -field RecordLength

The total length of a record, in bytes.

Because USN record is a variable size, the <b>RecordLength</b> member should be used when calculating the address of the next record in an output buffer, for example, a buffer that is returned from operations for the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function that work with different USN record types.

For <a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a>, the size in bytes of any change journal record is at most the size of the structure, plus (NumberOfExtents-1) times size of the <a href="https://msdn.microsoft.com/7D569FCB-06D4-4348-B75A-D087D1D37851">USN_RECORD_EXTENT</a>. 


### -field MajorVersion

The major version number of the change journal software for this record.

For example, if the change journal software is version 4.0, the major version number is 4.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>2</td>
<td>The structure is a <a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD_V2</a> structure and the remainder of the structure should be parsed using that layout.</td>
</tr>
<tr>
<td>3</td>
<td>The structure is a <a href="https://msdn.microsoft.com/6d95c5d1-6c6b-498f-a00d-eaa540e8b15b">USN_RECORD_V3</a> structure and the remainder of the structure should be parsed using that layout.</td>
</tr>
<tr>
<td>4</td>
<td>The structure is a <a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a> structure and the remainder of the structure should be parsed using that layout.</td>
</tr>
</table>
 


### -field MinorVersion

The minor version number of the change journal software for this record. For example, if the change journal software is version 4.0, the minor version number is zero. 


## -see-also




<a href="https://msdn.microsoft.com/7D569FCB-06D4-4348-B75A-D087D1D37851">USN_RECORD_EXTENT</a>



<a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD_V2</a>



<a href="https://msdn.microsoft.com/6d95c5d1-6c6b-498f-a00d-eaa540e8b15b">USN_RECORD_V3</a>



<a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

