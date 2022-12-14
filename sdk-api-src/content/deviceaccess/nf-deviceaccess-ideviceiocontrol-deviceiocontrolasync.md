---
UID: NF:deviceaccess.IDeviceIoControl.DeviceIoControlAsync
title: IDeviceIoControl::DeviceIoControlAsync (deviceaccess.h)
description: The DeviceIoControlAsync method sends an asynchronous device input/output (I/O) control request to the device interface that the call to the CreateDeviceAccessInstance function specified.
helpviewer_keywords: ["DeviceIoControlAsync","DeviceIoControlAsync method [Device Access Broker API]","DeviceIoControlAsync method [Device Access Broker API]","IDeviceIoControl interface","IDeviceIoControl interface [Device Access Broker API]","DeviceIoControlAsync method","IDeviceIoControl.DeviceIoControlAsync","IDeviceIoControl::DeviceIoControlAsync","deviceaccess.ideviceiocontrol_deviceiocontrolasync","deviceaccess/IDeviceIoControl::DeviceIoControlAsync"]
old-location: deviceaccess\ideviceiocontrol_deviceiocontrolasync.htm
tech.root: deviceaccess
ms.assetid: 550eadd0-c03b-40b3-9f08-639085365f4b
ms.date: 12/05/2018
ms.keywords: DeviceIoControlAsync, DeviceIoControlAsync method [Device Access Broker API], DeviceIoControlAsync method [Device Access Broker API],IDeviceIoControl interface, IDeviceIoControl interface [Device Access Broker API],DeviceIoControlAsync method, IDeviceIoControl.DeviceIoControlAsync, IDeviceIoControl::DeviceIoControlAsync, deviceaccess.ideviceiocontrol_deviceiocontrolasync, deviceaccess/IDeviceIoControl::DeviceIoControlAsync
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
 - IDeviceIoControl::DeviceIoControlAsync
 - deviceaccess/IDeviceIoControl::DeviceIoControlAsync
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
 - IDeviceIoControl.DeviceIoControlAsync
---

# IDeviceIoControl::DeviceIoControlAsync


## -description

The <b>DeviceIoControlAsync</b> method sends an asynchronous device input/output (I/O) control request to the device interface that the call to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a> function specified.

## -parameters

### -param ioControlCode [in]

The I/O control code for the operation.

### -param inputBuffer [in]

An optional input buffer for the operation.

### -param inputBufferSize [in]

The size of input buffer, in bytes.

### -param outputBuffer [out]

An operational output buffer for the operation.

### -param outputBufferSize [in]

The size of output buffer, in bytes.

### -param requestCompletionCallback [in]

The callback interface on which the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-idevicerequestcompletioncallback-requestcompletion">RequestCompletion</a> method is called if the operation is submitted successfully.

### -param cancelContext [out]

An optional pointer that receives a cancel context that can be passed to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-canceloperation">CancelOperation</a> method to cancel an outstanding request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the request is submitted successfully (that is, calling this function doesn't immediately return an error), the result of the operation is available in the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-idevicerequestcompletioncallback-requestcompletion">RequestCompletion</a> callback of the supplied <a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback">IDeviceRequestCompletionCallback</a> interface.

An operation that the system (operating system or device driver) fails immediately doesn't result in a callback.This means that the caller  receives a callback only if this function returns <b>S_OK</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-ideviceiocontrol">IDeviceIoControl</a>