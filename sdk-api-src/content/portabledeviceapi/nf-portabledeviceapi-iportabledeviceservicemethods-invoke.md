---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.Invoke
title: IPortableDeviceServiceMethods::Invoke (portabledeviceapi.h)
description: Synchronously invokes a method.
helpviewer_keywords: ["IPortableDeviceServiceMethods interface [Windows Portable Devices SDK]","Invoke method","IPortableDeviceServiceMethods.Invoke","IPortableDeviceServiceMethods::Invoke","Invoke","Invoke method [Windows Portable Devices SDK]","Invoke method [Windows Portable Devices SDK]","IPortableDeviceServiceMethods interface","portabledeviceapi/IPortableDeviceServiceMethods::Invoke","wpdsdk.iportabledeviceservicemethods_invoke"]
old-location: wpdsdk\iportabledeviceservicemethods_invoke.htm
tech.root: wpdsdk
ms.assetid: 9c972815-c95a-4718-abac-dcc28a2198e1
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],Invoke method, IPortableDeviceServiceMethods.Invoke, IPortableDeviceServiceMethods::Invoke, Invoke, Invoke method [Windows Portable Devices SDK], Invoke method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, portabledeviceapi/IPortableDeviceServiceMethods::Invoke, wpdsdk.iportabledeviceservicemethods_invoke
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceServiceMethods::Invoke
 - portabledeviceapi/IPortableDeviceServiceMethods::Invoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceMethods.Invoke
---

# IPortableDeviceServiceMethods::Invoke


## -description

The <b>Invoke</b> method synchronously invokes a method.

## -parameters

### -param Method [in]

The method to invoke.

### -param pParameters [in]

A pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the parameters of the invoked method, or <b>NULL</b> to indicate that the method has no parameters.

### -param ppResults [in, out]

The address of a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the method results, or <b>NULL</b> to ignore the method results.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

The method invocation is synchronous and will not return until the method has completed. For long-running methods, your application should call the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">InvokeAsync</a> method instead.


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/invoking-methods-synchronously">Invoking Service Methods</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods Interface</a>



<a href="/windows/desktop/wpd_sdk/invoking-methods-synchronously">Invoking Service Methods</a>