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

# IPortableDeviceServiceMethods::Cancel


## -description


The <b>Cancel</b> method cancels a pending method invocation.


## -parameters




### -param pCallback [in]

A pointer to the callback object whose method invocation is to be canceled, or <b>NULL</b> to cancel all pending method invocations.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



A callback object identifies a method invocation. If the same callback object is reused for multiple calls to the <a href="https://msdn.microsoft.com/0acf416c-4d59-4eb5-b1ce-aef848b54949">InvokeAsync</a> method, all method invocations arising from these calls will be cancelled.

To enable targeted cancellation of a specific method invocation, pass a unique instance of the <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> interface to the <a href="https://msdn.microsoft.com/0acf416c-4d59-4eb5-b1ce-aef848b54949">InvokeAsync</a> method.
  
  




## -see-also




<a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods Interface</a>
 

 

