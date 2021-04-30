---
UID: NF:deviceaccess.IDeviceIoControl.CancelOperation
title: IDeviceIoControl::CancelOperation (deviceaccess.h)
description: The CancelOperation method attempts to cancel a previously issued call by using the DeviceIoControlAsync method.
helpviewer_keywords: ["CancelOperation","CancelOperation method [Device Access Broker API]","CancelOperation method [Device Access Broker API]","IDeviceIoControl interface","IDeviceIoControl interface [Device Access Broker API]","CancelOperation method","IDeviceIoControl.CancelOperation","IDeviceIoControl::CancelOperation","deviceaccess.ideviceiocontrol_canceloperation","deviceaccess/IDeviceIoControl::CancelOperation"]
old-location: deviceaccess\ideviceiocontrol_canceloperation.htm
tech.root: deviceaccess
ms.assetid: 476a84c8-4065-4a4f-ad74-68cbbbabd5dd
ms.date: 12/05/2018
ms.keywords: CancelOperation, CancelOperation method [Device Access Broker API], CancelOperation method [Device Access Broker API],IDeviceIoControl interface, IDeviceIoControl interface [Device Access Broker API],CancelOperation method, IDeviceIoControl.CancelOperation, IDeviceIoControl::CancelOperation, deviceaccess.ideviceiocontrol_canceloperation, deviceaccess/IDeviceIoControl::CancelOperation
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
 - IDeviceIoControl::CancelOperation
 - deviceaccess/IDeviceIoControl::CancelOperation
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
 - IDeviceIoControl.CancelOperation
---

# IDeviceIoControl::CancelOperation


## -description

The <b>CancelOperation</b> method attempts to cancel a previously issued call by using the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a> method.

## -parameters

### -param cancelContext [in]

The cancel context that a previous call to <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a> returned.

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
The operation was still outstanding, and cancellation was attempted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operation was no longer outstanding.

</td>
</tr>
</table>

## -remarks

Regardless of whether cancellation is successful, the result of the operation is available in the callback that's provided to the asynchronous call.

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-ideviceiocontrol">IDeviceIoControl</a>