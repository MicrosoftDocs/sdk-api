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

# VOLUME_BITMAP_BUFFER structure


## -description


Represents the occupied and available clusters on a disk. This structure is the output buffer for the 
<a href="https://msdn.microsoft.com/80ef93ee-21a4-4766-82d2-d2ddef3ef5bb">FSCTL_GET_VOLUME_BITMAP</a> control code.


## -struct-fields




### -field StartingLcn

Starting LCN requested as an input to the operation.


### -field BitmapSize

The number of clusters on the volume, starting from the starting LCN returned in the <b>StartingLcn</b> member of this structure. See the following Remarks section for details.


### -field Buffer

Array of bytes containing the bitmap that the operation returns. The bitmap is bitwise from bit zero of the bitmap to the end. Thus, starting at the requested cluster, the bitmap goes from bit 0 of byte 0, bit 1 of byte 0 ... bit 7 of byte 0, bit 0 of byte 1, and so on. The value 1 indicates that the cluster is allocated (in use). The value 0 indicates that the cluster is not allocated (free). 


## -remarks



The <b>BitmapSize</b> member is the number of clusters on the volume starting from the starting LCN returned in the <b>StartingLcn</b> member of this structure. For example, suppose there are 0xD3F7 clusters on the volume. If you start the bitmap query at LCN 0xA007, then both the FAT and NTFS file systems will round down the returned starting LCN to LCN 0xA000. The value returned in the <b>BitmapSize</b> member will be (0xD3F7 – 0xA000), or 0x33F7.




## -see-also




<a href="https://msdn.microsoft.com/27ccaab7-ec89-489b-80dc-df9beb7969bc">Defragmentation</a>



<a href="https://msdn.microsoft.com/80ef93ee-21a4-4766-82d2-d2ddef3ef5bb">FSCTL_GET_VOLUME_BITMAP</a>
 

 

