---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Close
title: ICreateDeviceAccessAsync::Close (deviceaccess.h)
description: The Close method performs cleanup after the asynchronous operation is completed and you retrieve the results.
helpviewer_keywords: ["Close","Close method [Device Access Broker API]","Close method [Device Access Broker API]","ICreateDeviceAccessAsync interface","ICreateDeviceAccessAsync interface [Device Access Broker API]","Close method","ICreateDeviceAccessAsync.Close","ICreateDeviceAccessAsync::Close","deviceaccess.icreatedeviceaccessasync_close","deviceaccess/ICreateDeviceAccessAsync::Close"]
old-location: deviceaccess\icreatedeviceaccessasync_close.htm
tech.root: deviceaccess
ms.assetid: 58887745-6a36-4600-9a1b-f9709a0e37e8
ms.date: 12/05/2018
ms.keywords: Close, Close method [Device Access Broker API], Close method [Device Access Broker API],ICreateDeviceAccessAsync interface, ICreateDeviceAccessAsync interface [Device Access Broker API],Close method, ICreateDeviceAccessAsync.Close, ICreateDeviceAccessAsync::Close, deviceaccess.icreatedeviceaccessasync_close, deviceaccess/ICreateDeviceAccessAsync::Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateDeviceAccessAsync::Close
 - deviceaccess/ICreateDeviceAccessAsync::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Deviceaccess.lib
 - Deviceaccess.dll
api_name:
 - ICreateDeviceAccessAsync.Close
---

# ICreateDeviceAccessAsync::Close


## -description

The <b>Close</b> method performs cleanup  after the asynchronous operation is completed and you retrieve the results.



## -returns

This method supports standard return values, in addition to these:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The property value was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The operation did not finish.

</td>
</tr>
</table>

## -remarks

If the binding is successful, it doesn't invalidate the interface that the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult">GetResult</a> method returns.

It isn't strictly necessary to call this method, because resources are cleaned up when the underlying object is deleted. But doing so allows the system to free up resources that are associated with the asynchronous binding. As such, it's good practice to call <b>Close</b> after you retrieve the results.

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a>
