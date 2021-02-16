---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.Wait
title: ICreateDeviceAccessAsync::Wait (deviceaccess.h)
description: The Wait method waits a specified length of time for an asynchronous bind operation that is in progress to finish.
helpviewer_keywords: ["ICreateDeviceAccessAsync interface [Device Access Broker API]","Wait method","ICreateDeviceAccessAsync.Wait","ICreateDeviceAccessAsync::Wait","Wait","Wait method [Device Access Broker API]","Wait method [Device Access Broker API]","ICreateDeviceAccessAsync interface","deviceaccess.icreatedeviceaccessasync_wait","deviceaccess/ICreateDeviceAccessAsync::Wait"]
old-location: deviceaccess\icreatedeviceaccessasync_wait.htm
tech.root: deviceaccess
ms.assetid: 6fdab230-f8f7-47fa-838f-97316a4e78b9
ms.date: 12/05/2018
ms.keywords: ICreateDeviceAccessAsync interface [Device Access Broker API],Wait method, ICreateDeviceAccessAsync.Wait, ICreateDeviceAccessAsync::Wait, Wait, Wait method [Device Access Broker API], Wait method [Device Access Broker API],ICreateDeviceAccessAsync interface, deviceaccess.icreatedeviceaccessasync_wait, deviceaccess/ICreateDeviceAccessAsync::Wait
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
 - ICreateDeviceAccessAsync::Wait
 - deviceaccess/ICreateDeviceAccessAsync::Wait
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
 - ICreateDeviceAccessAsync.Wait
---

# ICreateDeviceAccessAsync::Wait


## -description

The <b>Wait</b> method waits a specified length of time for an asynchronous bind operation that is in progress to finish.

## -parameters

### -param timeout [in]

Timeout value, in milliseconds, for the wait call. Use <b>INFINITE</b> if you want the caller to wait until the operation finishes.

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
The wait was successful and the operation finished.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The wait timed out before the operation finished.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The operation has already closed when this method was called.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a>