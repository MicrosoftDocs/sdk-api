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

# RETRIEVAL_POINTERS_BUFFER structure


## -description


Contains the output for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a> control code.


## -struct-fields




### -field ExtentCount

The count of elements in the <b>Extents</b> array.


### -field StartingVcn

The starting VCN returned by the function call. This is not necessarily the VCN requested by the function call, as the file system driver may round down to the first VCN of the extent in which the requested starting VCN is found.


### -field NextVcn

 


### -field Lcn

 


### -field Extents

Array of <b>Extents</b> structures. For the number of members in the array, see <b>ExtentCount</b>. Each member of the array has the following members.



#### NextVcn

The VCN at which the next extent begins. This value minus either <b>StartingVcn</b> (for the first <b>Extents</b> array member) or the <b>NextVcn</b> of the previous member of the array (for all other <b>Extents</b> array members) is the length, in clusters, of the current extent. The length is an input to the <a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a> operation.



#### Lcn

The LCN at which the current extent begins on the volume. This value is an input to the <a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a> operation. On the NTFS file system, the value (LONGLONG) –1 indicates either a compression unit that is partially allocated, or an unallocated region of a sparse file.


## -see-also




<a href="https://msdn.microsoft.com/27ccaab7-ec89-489b-80dc-df9beb7969bc">Defragmentation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a>



<a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a>
 

 

