---
UID: NN:deviceaccess.ICreateDeviceAccessAsync
title: ICreateDeviceAccessAsync (deviceaccess.h)
description: The ICreateDeviceAccessAsync interface is returned from a call to CreateDeviceAccessInstance.
old-location: deviceaccess\icreatedeviceaccessasync.htm
tech.root: deviceaccess
ms.assetid: ebc8d694-c933-4d98-95f5-67b0dd733d4d
ms.date: 12/05/2018
ms.keywords: ICreateDeviceAccessAsync, ICreateDeviceAccessAsync interface [Device Access Broker API], ICreateDeviceAccessAsync interface [Device Access Broker API],described, deviceaccess.icreatedeviceaccessasync, deviceaccess/ICreateDeviceAccessAsync
f1_keywords:
- deviceaccess/ICreateDeviceAccessAsync
dev_langs:
- c++
req.header: deviceaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Deviceaccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Deviceaccess.lib
- Deviceaccess.dll
api_name:
- ICreateDeviceAccessAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateDeviceAccessAsync interface


## -description


The <b>ICreateDeviceAccessAsync</b> interface is returned from a call to CreateDeviceAccessInstance. It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateDeviceAccessAsync</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateDeviceAccessAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateDeviceAccessAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Attempts to cancel an asynchronous operation that  is in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-close">Close</a>
</td>
<td align="left" width="63%">
Performs cleanup after completion of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult">GetResult</a>
</td>
<td align="left" width="63%">
Retrieves the result of an asynchronous bind operation for a CreateDeviceAccessInstance call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait">Wait</a>
</td>
<td align="left" width="63%">
Waits a specified length of time for an asynchronous bind operation that is in progress to finish.

</td>
</tr>
</table> 

