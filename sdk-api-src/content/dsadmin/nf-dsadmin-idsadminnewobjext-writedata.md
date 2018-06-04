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

# IDsAdminNewObjExt::WriteData


## -description


The <b>IDsAdminNewObjExt::WriteData</b> method enables the object creation wizard extension to write its data into an object in Active Directory Domain Services.


## -parameters




### -param hWnd [in]

The window handle used as the parent window for possible error messages.


### -param uContext [in]

Specifies the context in which <b>WriteData</b> is called. This will be one of the following values.



#### DSA_NEWOBJ_CTX_PRECOMMIT

<b>WriteData</b> is called prior to the new object committed to persistent storage. This is the context during which a secondary object creation extension should write its data.



#### DSA_NEWOBJ_CTX_POSTCOMMIT

<b>WriteData</b> is called after the new object has been committed to persistent storage.



#### DSA_NEWOBJ_CTX_CLEANUP

There has been a failure during the write process of the temporary object and the temporary object is recreated.


## -returns



Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise.




## -remarks



A pointer to the temporary directory object is supplied to the extension when the <a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a> method is called.

A secondary object creation extension should not commit the data set during the <b>WriteData</b> method by calling <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>. The primary object creation extension will commit all of the data for the object when all of the extensions have added their data.




## -see-also




<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a>
 

 

