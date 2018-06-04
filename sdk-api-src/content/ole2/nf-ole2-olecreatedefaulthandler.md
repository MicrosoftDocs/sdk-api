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

# OleCreateDefaultHandler function


## -description


Creates a new instance of the default embedding handler. This instance is initialized so it creates a local server when the embedded object enters the running state. 




## -parameters




### -param clsid [in]

CLSID identifying the OLE server to be loaded when the embedded object enters the running state.


### -param pUnkOuter [in]

 Pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface if the handler is to be aggregated; <b>NULL</b> if it is not to be aggregated.


### -param riid [in]

Reference to the identifier of the interface, usually IID_IOleObject, through which the caller will communicate with the handler.


### -param lplpObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created handler.


## -returns



This function returns NOERROR on success and supports the standard return value E_OUTOFMEMORY.




## -remarks



<b>OleCreateDefaultHandler</b> creates a new instance of the default embedding handler, initialized so it creates a local server identified by the <i>clsid</i> parameter when the embedded object enters the running state. If you are writing a handler and want to use the services of the default handler, call <b>OleCreateDefaultHandler</b>. OLE also calls it internally when the CLSID specified in an object creation call is not registered.



If the given class does not have a special handler, a call to <b>OleCreateDefaultHandler</b> produces the same results as a call to the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function with the class context parameter assigned the value CLSCTX_INPROC_HANDLER.





## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>
 

 

