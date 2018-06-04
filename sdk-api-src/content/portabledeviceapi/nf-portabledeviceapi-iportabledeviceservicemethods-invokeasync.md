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

# IPortableDeviceServiceMethods::InvokeAsync


## -description


The <b>InvokeAsync</b> method asynchronously invokes a method.


## -parameters




### -param Method [in]

The method to invoke.


### -param pParameters [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains the parameters of the invoked method, or <b>NULL</b> to indicate that the method has no parameters.


### -param pCallback [in]

A pointer to an application-supplied <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> callback object that  receives the method results, or <b>NULL</b> to ignore the method results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



When invoking multiple methods, clients can create a separate instance of the <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> interface for each invocation, saving a context with that instance object before passing it to the <b>InvokeAsync</b> method. This way, the method operation can be identified when the <a href="https://msdn.microsoft.com/b04e7bf1-bad7-4e9a-b53a-ec064d323f94">OnComplete</a>  method is called. Use of a unique object for each invocation also allows targeted cancellation of an operation by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> method.
  


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/d3072e34-65f2-4eeb-bcfa-e2db2d34e680">Invoking Service Methods Asynchronously</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods Interface</a>



<a href="https://msdn.microsoft.com/d3072e34-65f2-4eeb-bcfa-e2db2d34e680">Invoking Service Methods Asynchronously</a>
 

 

