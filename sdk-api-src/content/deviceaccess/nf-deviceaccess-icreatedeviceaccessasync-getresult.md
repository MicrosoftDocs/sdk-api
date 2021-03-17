---
UID: NF:deviceaccess.ICreateDeviceAccessAsync.GetResult
title: ICreateDeviceAccessAsync::GetResult (deviceaccess.h)
description: Retrieves an IDeviceIoControl object that's bound to the device interface that's specified in a call to the CreateDeviceAccessInstance function.
helpviewer_keywords: ["GetResult","GetResult method [Device Access Broker API]","GetResult method [Device Access Broker API]","ICreateDeviceAccessAsync interface","ICreateDeviceAccessAsync interface [Device Access Broker API]","GetResult method","ICreateDeviceAccessAsync.GetResult","ICreateDeviceAccessAsync::GetResult","deviceaccess.icreatedeviceaccessasync_getresult","deviceaccess/ICreateDeviceAccessAsync::GetResult"]
old-location: deviceaccess\icreatedeviceaccessasync_getresult.htm
tech.root: deviceaccess
ms.assetid: 002e6638-a38a-4fda-b71c-a7a6983dda62
ms.date: 12/05/2018
ms.keywords: GetResult, GetResult method [Device Access Broker API], GetResult method [Device Access Broker API],ICreateDeviceAccessAsync interface, ICreateDeviceAccessAsync interface [Device Access Broker API],GetResult method, ICreateDeviceAccessAsync.GetResult, ICreateDeviceAccessAsync::GetResult, deviceaccess.icreatedeviceaccessasync_getresult, deviceaccess/ICreateDeviceAccessAsync::GetResult
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
 - ICreateDeviceAccessAsync::GetResult
 - deviceaccess/ICreateDeviceAccessAsync::GetResult
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
 - ICreateDeviceAccessAsync.GetResult
---

# ICreateDeviceAccessAsync::GetResult


## -description

Retrieves an <a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-ideviceiocontrol">IDeviceIoControl</a> object that's bound to the device interface that's specified in a call to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a> function.

## -parameters

### -param riid [in]

An interface identifier that indicates what type of device access interface the caller wants to retrieve. The only valid value for this identifier is IID_IDeviceIoControl.

### -param deviceAccess [out]

If the binding was successful, contains an interface of the type that was supplied to the initial call to <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a>.

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
The binding was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation wasn't in a valid state. The bind operation was either still in progress or not yet started.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a>