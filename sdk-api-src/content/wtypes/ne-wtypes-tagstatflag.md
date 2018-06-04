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

# tagSTATFLAG enumeration


## -description



			The 
<b>STATFLAG</b> enumeration values indicate whether the method should try to return a name in the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure. The values are used in the 
<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>, 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>, and 
<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> methods to save memory when the <b>pwcsName</b> member is not required.


## -enum-fields




### -field STATFLAG_DEFAULT

Requests that the statistics include the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure.


### -field STATFLAG_NONAME

Requests that the statistics not include the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure. If the name is omitted, there is no need for the 
<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>, 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>, and 
<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> methods methods to allocate and free memory for the string value of the name, therefore the method reduces time and resources used in an allocation and free operation.


### -field STATFLAG_NOOPEN

Not implemented.


## -see-also




<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>



<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a>
 

 

