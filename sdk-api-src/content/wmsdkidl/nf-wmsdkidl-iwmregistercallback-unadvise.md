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

# IWMRegisterCallback::Unadvise


## -description



The <b>Unadvise</b> method unregisters the application's <b>IWMStatusCallback</b> callback interface. Call this method when the application has finished using the sink object. It notifies the object to stop sending status events to the application.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> interface of an object.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3831b727-7fdc-4d05-a7b3-86ca5b5c3b17">IWMRegisterCallback Interface</a>



<a href="https://msdn.microsoft.com/69d12e5c-23fd-4d4b-959e-fe7979bf3fdb">IWMRegisterCallback::Advise</a>
 

 

