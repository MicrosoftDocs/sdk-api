---
UID: NN:portabledeviceapi.IPortableDeviceServiceMethods
title: IPortableDeviceServiceMethods (portabledeviceapi.h)
author: windows-sdk-content
description: Invokes, or cancels invocation of, a method on a service.
old-location: wpdsdk\iportabledeviceservicemethods.htm
tech.root: wpd_sdk
ms.assetid: 9d233dea-91b6-4358-830c-6abe466264e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethods, IPortableDeviceServiceMethods interface [Windows Portable Devices SDK], IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceMethods, wpdsdk.iportabledeviceservicemethods
ms.topic: interface
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceServiceMethods"
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
 - IPortableDeviceServiceMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceMethods interface


## -description


The <b>IPortableDeviceServiceMethods</b> interface invokes, or cancels invocation of, a method on a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceMethods</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceServiceMethods</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceServiceMethods</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending method invocation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Synchronously invokes a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">InvokeAsync</a>
</td>
<td align="left" width="63%">
Asynchronously invokes a method.

</td>
</tr>
</table> 

