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

# _MERGE_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD) merge request parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/1f542a51-d314-4add-a389-d450785b0a73">MERGE_VIRTUAL_DISK_VERSION</a> enumeration 
      that specifies the version of the 
      <b>MERGE_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the VHD functions.


### -field Version1

This structure is used when the Version member is <b>MERGE_VIRTUAL_DISK_VERSION_1</b> 
       (1).


### -field Version1.MergeDepth

Depth of the merge request. This is the number of parent disks in the differencing chain to merge 
         together.

<div class="alert"><b>Note</b>  The RWDepth of the virtual disk must be greater than <b>MergeDepth</b>. For more 
         information, see 
         <a href="https://msdn.microsoft.com/ad67bc3e-a0fe-4198-9307-819577abef7f">OPEN_VIRTUAL_DISK_PARAMETERS</a>.</div>
<div> </div>

### -field Version2

This structure is used when the Version member is <b>MERGE_VIRTUAL_DISK_VERSION_2</b> 
        (2).

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported until Windows 8 and Windows Server 2012.


### -field Version2.MergeSourceDepth

Depth from the leaf from which to begin the merge.  The leaf is at depth 1.


### -field Version2.MergeTargetDepth

Depth from  the leaf to target the merge.  The leaf is at depth 1.


## -remarks



The depth of a merge request specified by the <b>MergeDepth</b> member is the number of  
    parent VHD image files in the differencing chain to be merged.  For more information, see 
    <a href="https://msdn.microsoft.com/9a9068d1-2f81-42a2-a3b2-6030a24a4445">MergeVirtualDisk</a>.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/9a9068d1-2f81-42a2-a3b2-6030a24a4445">MergeVirtualDisk</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

