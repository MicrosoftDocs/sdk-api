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

# IDsAdminNewObjExt::OnError


## -description


The <b>IDsAdminNewObjExt::OnError</b> method is called when an error has occurred in the wizard pages.


## -parameters




### -param hWnd [in]

The window handle used as the parent window for possible error messages.


### -param hr [in]

<b>HRESULT</b> of the error that occurred.


### -param uContext [in]

Specifies the context in which <b>OnError</b> is called. This will be one of the following values.



#### DSA_NEWOBJ_CTX_PRECOMMIT

An error occurred prior to the new object committed to persistent storage.



#### DSA_NEWOBJ_CTX_COMMIT

An error occurred while the new object was committed to persistent storage.



#### DSA_NEWOBJ_CTX_POSTCOMMIT

An error occurred after the new object was committed to persistent storage.



#### DSA_NEWOBJ_CTX_CLEANUP

An error occurred while the new object was committed to persistent storage.


## -returns



A primary creation extension returns <b>S_OK</b> to indicate that the error was handled by the extension or an OLE-defined error code to cause the system to display an error message.

The return value is ignored for a secondary creation extension.




## -see-also




<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>
 

 

