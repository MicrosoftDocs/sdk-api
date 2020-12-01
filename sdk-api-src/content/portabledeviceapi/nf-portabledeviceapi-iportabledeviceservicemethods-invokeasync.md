---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.InvokeAsync
title: IPortableDeviceServiceMethods::InvokeAsync (portabledeviceapi.h)
description: Asynchronously invokes a method.
helpviewer_keywords: ["IPortableDeviceServiceMethods interface [Windows Portable Devices SDK]","InvokeAsync method","IPortableDeviceServiceMethods.InvokeAsync","IPortableDeviceServiceMethods::InvokeAsync","InvokeAsync","InvokeAsync method [Windows Portable Devices SDK]","InvokeAsync method [Windows Portable Devices SDK]","IPortableDeviceServiceMethods interface","portabledeviceapi/IPortableDeviceServiceMethods::InvokeAsync","wpdsdk.iportabledeviceservicemethods_invokeasync"]
old-location: wpdsdk\iportabledeviceservicemethods_invokeasync.htm
tech.root: wpdsdk
ms.assetid: 0acf416c-4d59-4eb5-b1ce-aef848b54949
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],InvokeAsync method, IPortableDeviceServiceMethods.InvokeAsync, IPortableDeviceServiceMethods::InvokeAsync, InvokeAsync, InvokeAsync method [Windows Portable Devices SDK], InvokeAsync method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, portabledeviceapi/IPortableDeviceServiceMethods::InvokeAsync, wpdsdk.iportabledeviceservicemethods_invokeasync
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
 - IPortableDeviceServiceMethods::InvokeAsync
 - portabledeviceapi/IPortableDeviceServiceMethods::InvokeAsync
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
 - IPortableDeviceServiceMethods.InvokeAsync
---

# IPortableDeviceServiceMethods::InvokeAsync


## -description

The <b>InvokeAsync</b> method asynchronously invokes a method.

## -parameters

### -param Method [in]

The method to invoke.

### -param pParameters [in]

A pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the parameters of the invoked method, or <b>NULL</b> to indicate that the method has no parameters.

### -param pCallback [in]

A pointer to an application-supplied <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback">IPortableDeviceServiceMethodCallback</a> callback object that  receives the method results, or <b>NULL</b> to ignore the method results.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

When invoking multiple methods, clients can create a separate instance of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback">IPortableDeviceServiceMethodCallback</a> interface for each invocation, saving a context with that instance object before passing it to the <b>InvokeAsync</b> method. This way, the method operation can be identified when the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete">OnComplete</a>  method is called. Use of a unique object for each invocation also allows targeted cancellation of an operation by the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-cancel">Cancel</a> method.
  


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/invoking-methods-asynchronously">Invoking Service Methods Asynchronously</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods Interface</a>



<a href="/windows/desktop/wpd_sdk/invoking-methods-asynchronously">Invoking Service Methods Asynchronously</a>