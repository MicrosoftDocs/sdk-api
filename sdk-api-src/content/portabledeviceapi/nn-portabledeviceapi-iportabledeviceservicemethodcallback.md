---
UID: NN:portabledeviceapi.IPortableDeviceServiceMethodCallback
title: IPortableDeviceServiceMethodCallback (portabledeviceapi.h)
description: Contains a method that applications use to track the completion of a callback method. Applications that call service methods asynchronously may implement this interface, and supply it as a parameter to IPortableDeviceServiceMethods::InvokeAsync.
helpviewer_keywords: ["IPortableDeviceServiceMethodCallback","IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK]","IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK]","described","portabledeviceapi/IPortableDeviceServiceMethodCallback","wpdsdk.iportabledeviceservicemethodcallback"]
old-location: wpdsdk\iportabledeviceservicemethodcallback.htm
tech.root: wpdsdk
ms.assetid: cda7e4f7-0006-4b87-ac68-d07004440ce8
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethodCallback, IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK], IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceMethodCallback, wpdsdk.iportabledeviceservicemethodcallback
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
 - IPortableDeviceServiceMethodCallback
 - portabledeviceapi/IPortableDeviceServiceMethodCallback
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
 - IPortableDeviceServiceMethodCallback
---

# IPortableDeviceServiceMethodCallback interface


## -description

The <b>IPortableDeviceServiceMethodCallback</b> interface contains a method that applications use to track the completion of a callback method.  Applications that call service methods asynchronously may implement this interface, and supply it as a parameter to <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">IPortableDeviceServiceMethods::InvokeAsync</a>. 

Each asynchronous method invocation uses the application-supplied callback object as its context. Therefore, an application that intends to simultaneously invoke multiple methods should avoid reusing the callback object. Instead, the application should provide a unique instance of the callback object for each call to <b>InvokeAsync</b>

## -inheritance

The <b>IPortableDeviceServiceMethodCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceServiceMethodCallback</b> also has these types of members:

