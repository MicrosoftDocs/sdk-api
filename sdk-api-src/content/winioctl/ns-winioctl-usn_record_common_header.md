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
 

 

