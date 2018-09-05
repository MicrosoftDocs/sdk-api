---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.InvokeAsync
title: IPortableDeviceServiceMethods::InvokeAsync
author: windows-sdk-content
description: Asynchronously invokes a method.
old-location: wpdsdk\iportabledeviceservicemethods_invokeasync.htm
old-project: wpd_sdk
ms.assetid: 0acf416c-4d59-4eb5-b1ce-aef848b54949
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],InvokeAsync method, IPortableDeviceServiceMethods.InvokeAsync, IPortableDeviceServiceMethods::InvokeAsync, InvokeAsync, InvokeAsync method [Windows Portable Devices SDK], InvokeAsync method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, portabledeviceapi/IPortableDeviceServiceMethods::InvokeAsync, wpdsdk.iportabledeviceservicemethods_invokeasync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceMethods.InvokeAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceServiceMethods::InvokeAsync


## -description


The <b>InvokeAsync</b> method asynchronously invokes a method.


## -parameters




### -param Method [in]

The method to invoke.


### -param pParameters [in]

A pointer to an <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that contains the parameters of the invoked method, or <b>NULL</b> to indicate that the method has no parameters.


### -param pCallback [in]

A pointer to an application-supplied <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> callback object that  receives the method results, or <b>NULL</b> to ignore the method results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



When invoking multiple methods, clients can create a separate instance of the <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> interface for each invocation, saving a context with that instance object before passing it to the <b>InvokeAsync</b> method. This way, the method operation can be identified when the <a href="https://msdn.microsoft.com/b04e7bf1-bad7-4e9a-b53a-ec064d323f94">OnComplete</a>  method is called. Use of a unique object for each invocation also allows targeted cancellation of an operation by the <a href="https://msdn.microsoft.com/03281c4f-4dba-4ac4-af5d-d700c914ed01">Cancel</a> method.
  


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/d3072e34-65f2-4eeb-bcfa-e2db2d34e680">Invoking Service Methods Asynchronously</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods Interface</a>



<a href="https://msdn.microsoft.com/d3072e34-65f2-4eeb-bcfa-e2db2d34e680">Invoking Service Methods Asynchronously</a>
 

 

