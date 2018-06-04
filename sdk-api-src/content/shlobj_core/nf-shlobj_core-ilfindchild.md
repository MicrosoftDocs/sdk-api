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

# ILFindChild function


## -description


Determines whether a specified <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure is the child of another <b>ITEMIDLIST</b> structure.


## -parameters




### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the parent <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pidlChild [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -returns



Type: <b>PUIDLIST_RELATIVE</b>

Returns a pointer to the child's simple <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure if <i>pidlChild</i> is a child of <i>pidlParent</i>. The returned structure consists of <i>pidlChild</i>, minus the <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structures that make up <i>pidlParent</i>. Returns <b>NULL</b> if <i>pidlChild</i> is not a child of <i>pidlParent</i>.

<div class="alert"><b>Note</b>  The returned pointer is a pointer into the existing parent structure. It is an alias for <i>pidlChild</i>. No new memory is allocated in association with the returned pointer. It is not the caller's responsibility to free the returned value.</div>
<div> </div>


