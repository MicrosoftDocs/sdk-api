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

# IRichEditOle::InsertObject


## -description


Inserts an object into a rich edit control.


## -parameters




### -param lpreobject

Type: <b><a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a>*</b>

The object information and interfaces. The rich edit control automatically increments the reference count for the interfaces if it holds onto them, so the caller can safely release the interfaces if they are not needed. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_OUTOFMEMORY is returned if memory could not be allocated to insert the object.




## -remarks



If the <b>cp</b> member of the <a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a> structure is REO_CP_SELECTION, the selection is replaced with the specified object.
	




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>



<a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a>



<b>Reference</b>
 

 

