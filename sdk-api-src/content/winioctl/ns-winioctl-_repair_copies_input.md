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

# _REPAIR_COPIES_INPUT structure


## -description


Input structure for the <a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a> control code. It describes a single block of data and indicates which of the copies is to be copied to the specified copies of the data. The 


## -struct-fields




### -field Size

Set to <code>sizeof(REPAIR_COPIES_INPUT)</code>.


### -field Flags

Reserved (must be zero)


### -field FileOffset

The file position to start the repair operation.


### -field Length

The number of bytes to be repaired.


### -field SourceCopy

The zero-based copy number of the source copy.


### -field NumberOfRepairCopies

The number of copies that will be repaired. This is the size of the <b>RepairCopies</b> 
      array.


### -field RepairCopies

The zero-based copy numbers of the copies that will be repaired.


## -see-also




<a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a>



<a href="https://msdn.microsoft.com/a3da7779-92e7-40bf-a889-dd2013e942ab">REPAIR_COPIES_OUTPUT</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

