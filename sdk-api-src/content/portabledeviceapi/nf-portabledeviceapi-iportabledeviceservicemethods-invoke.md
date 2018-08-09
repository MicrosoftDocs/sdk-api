---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.Invoke
title: IPortableDeviceServiceMethods::Invoke
author: windows-sdk-content
description: Synchronously invokes a method.
old-location: wpdsdk\iportabledeviceservicemethods_invoke.htm
old-project: wpd_sdk
ms.assetid: 9c972815-c95a-4718-abac-dcc28a2198e1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],Invoke method, IPortableDeviceServiceMethods.Invoke, IPortableDeviceServiceMethods::Invoke, Invoke, Invoke method [Windows Portable Devices SDK], Invoke method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, portabledeviceapi/IPortableDeviceServiceMethods::Invoke, wpdsdk.iportabledeviceservicemethods_invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
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
 - IPortableDeviceServiceMethods.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceServiceMethods::Invoke


## -description


The <b>Invoke</b> method synchronously invokes a method.


## -parameters




### -param Method [in]

The method to invoke.


### -param pParameters [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains the parameters of the invoked method, or <b>NULL</b> to indicate that the method has no parameters.


### -param ppResults [in, out]

The address of a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that receives the method results, or <b>NULL</b> to ignore the method results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



The method invocation is synchronous and will not return until the method has completed. For long-running methods, your application should call the <a href="https://msdn.microsoft.com/0acf416c-4d59-4eb5-b1ce-aef848b54949">InvokeAsync</a> method instead.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/3a2796c8-1a39-49eb-98e1-c9e06c61f397">Invoking Service Methods</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods Interface</a>



<a href="https://msdn.microsoft.com/3a2796c8-1a39-49eb-98e1-c9e06c61f397">Invoking Service Methods</a>
 

 

