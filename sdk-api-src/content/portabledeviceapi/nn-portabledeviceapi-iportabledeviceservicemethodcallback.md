---
UID: NN:portabledeviceapi.IPortableDeviceServiceMethodCallback
title: IPortableDeviceServiceMethodCallback (portabledeviceapi.h)
description: Contains a method that applications use to track the completion of a callback method. Applications that call service methods asynchronously may implement this interface, and supply it as a parameter to IPortableDeviceServiceMethods::InvokeAsync.
old-location: wpdsdk\iportabledeviceservicemethodcallback.htm
tech.root: wpd_sdk
ms.assetid: cda7e4f7-0006-4b87-ac68-d07004440ce8
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethodCallback, IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK], IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceMethodCallback, wpdsdk.iportabledeviceservicemethodcallback
ms.topic: interface
f1_keywords:
- portabledeviceapi/IPortableDeviceServiceMethodCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- PortableDeviceAPI.h
api_name:
- IPortableDeviceServiceMethodCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceMethodCallback interface


## -description


The <b>IPortableDeviceServiceMethodCallback</b> interface contains a method that applications use to track the completion of a callback method.  Applications that call service methods asynchronously may implement this interface, and supply it as a parameter to <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">IPortableDeviceServiceMethods::InvokeAsync</a>. 

Each asynchronous method invocation uses the application-supplied callback object as its context. Therefore, an application that intends to simultaneously invoke multiple methods should avoid reusing the callback object. Instead, the application should provide a unique instance of the callback object for each call to <b>InvokeAsync</b>


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceMethodCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceServiceMethodCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceServiceMethodCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete">OnComplete</a>
</td>
<td align="left" width="63%">
Indicates that a callback method has completed execution.

</td>
</tr>
</table> 

