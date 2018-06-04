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

# _REPARSE_GUID_DATA_BUFFER structure


## -description


Contains information about a reparse point. It is used by the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544836">FSCTL_GET_REPARSE_POINT</a> control code.


## -struct-fields




### -field ReparseTag

The reparse point tag. This member identifies the structure of the user-defined reparse data. For more 
      information, see <a href="https://msdn.microsoft.com/d02a2f50-d374-4149-bc04-49b7db052f62">Reparse Point Tags</a>.


### -field ReparseDataLength

The size of the reparse data in the <b>DataBuffer</b> member, in bytes. This value may 
      vary with different tags and may vary between two uses of the same tag.


### -field Reserved

Reserved; do not use.


### -field ReparseGuid

A <b>GUID</b> that uniquely identifies the  reparse point. When setting a reparse 
      point, the application must provide a non-NULL <b>GUID</b> in the 
      <b>ReparseGuid</b> member. When retrieving a reparse point from the file system, 
      <b>ReparseGuid</b> is the <b>GUID</b> assigned when the reparse point 
      was set. 
     


### -field GenericReparseBuffer


### -field GenericReparseBuffer.DataBuffer

The user-defined data for the reparse point. The contents are determined by the reparse point implementer. 
       The tag in the <b>ReparseTag</b> member and the <b>GUID</b> in the 
       <b>ReparseGuid</b> member indicate how the data is to be interpreted.


## -remarks



The <b>REPARSE_GUID_DATA_BUFFER</b> structure is 
    used by all third-party layered drivers to store data for a reparse point. Each reparse point contains one 
    instance of a <b>REPARSE_GUID_DATA_BUFFER</b> 
    structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544836">FSCTL_GET_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">Reparse Points</a>
 

 

