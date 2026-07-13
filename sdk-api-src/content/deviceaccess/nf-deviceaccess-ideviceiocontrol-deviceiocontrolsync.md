---
UID: NF:deviceaccess.IDeviceIoControl.DeviceIoControlSync
title: IDeviceIoControl::DeviceIoControlSync (deviceaccess.h)
description: The DeviceIoControlSync method sends a synchronous device input/output (I/O) control request to the device interface that the call to the CreateDeviceAccessInstance function specified.
helpviewer_keywords: ["DeviceIoControlSync","DeviceIoControlSync method [Device Access Broker API]","DeviceIoControlSync method [Device Access Broker API]","IDeviceIoControl interface","IDeviceIoControl interface [Device Access Broker API]","DeviceIoControlSync method","IDeviceIoControl.DeviceIoControlSync","IDeviceIoControl::DeviceIoControlSync","deviceaccess.ideviceiocontrol_deviceiocontrolsync","deviceaccess/IDeviceIoControl::DeviceIoControlSync"]
old-location: deviceaccess\ideviceiocontrol_deviceiocontrolsync.htm
tech.root: deviceaccess
ms.assetid: 7b17ab14-e9bb-40be-a463-ca9031ba9bb3
ms.date: 12/05/2018
ms.keywords: DeviceIoControlSync, DeviceIoControlSync method [Device Access Broker API], DeviceIoControlSync method [Device Access Broker API],IDeviceIoControl interface, IDeviceIoControl interface [Device Access Broker API],DeviceIoControlSync method, IDeviceIoControl.DeviceIoControlSync, IDeviceIoControl::DeviceIoControlSync, deviceaccess.ideviceiocontrol_deviceiocontrolsync, deviceaccess/IDeviceIoControl::DeviceIoControlSync
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
 - IDeviceIoControl::DeviceIoControlSync
 - deviceaccess/IDeviceIoControl::DeviceIoControlSync
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
 - IDeviceIoControl.DeviceIoControlSync
---

# IDeviceIoControl::DeviceIoControlSync


## -description

The <b>DeviceIoControlSync</b> method sends a synchronous device input/output (I/O) control request to the device interface that the call to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a> function specified.

## -parameters

### -param ioControlCode [in]

The I/O control code for the operation.

### -param inputBuffer [in]

An optional input buffer for the operation.

### -param inputBufferSize [in]

The size of input buffer, in bytes.

### -param outputBuffer [out]

An optional output buffer for the operation.

### -param outputBufferSize [in]

The size of output buffer, in bytes.

### -param bytesReturned [out]

A pointer to a variable that receives the number of bytes that were written into the output buffer, if one was specified.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Because  this is a synchronous method, you must not use it on a thread that can't handle being blocked for an extended period. In this case, you use the <b>DeviceIoControlAsync</b> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-ideviceiocontrol">IDeviceIoControl</a>