---
UID: NF:deviceaccess.IDeviceIoControl.DeviceIoControlAsync
title: IDeviceIoControl::DeviceIoControlAsync
author: windows-sdk-content
description: The DeviceIoControlAsync method sends an asynchronous device input/output (I/O) control request to the device interface that the call to the CreateDeviceAccessInstance function specified.
old-location: deviceaccess\ideviceiocontrol_deviceiocontrolasync.htm
old-project: deviceaccess
ms.assetid: 550eadd0-c03b-40b3-9f08-639085365f4b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DeviceIoControlAsync, DeviceIoControlAsync method [Device Access Broker API], DeviceIoControlAsync method [Device Access Broker API],IDeviceIoControl interface, IDeviceIoControl interface [Device Access Broker API],DeviceIoControlAsync method, IDeviceIoControl.DeviceIoControlAsync, IDeviceIoControl::DeviceIoControlAsync, deviceaccess.ideviceiocontrol_deviceiocontrolasync, deviceaccess/IDeviceIoControl::DeviceIoControlAsync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: deviceaccess.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VIDEOMEMORYINFO
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
product: Windows
targetos: Windows
req.lib: Deviceaccess.lib
req.dll: 
req.irql: 
---

# IDeviceIoControl::DeviceIoControlAsync


## -description


The <b>DeviceIoControlAsync</b> method sends an asynchronous device input/output (I/O) control request to the device interface that the call to the <a href="https://msdn.microsoft.com/082d6297-20ac-4557-8205-0451482a5758">CreateDeviceAccessInstance</a> function specified.


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

The callback interface on which the <a href="https://msdn.microsoft.com/5cc7bd36-3b8f-40af-badc-e8fc16d4a4c5">RequestCompletion</a> method is called if the operation is submitted successfully.


### -param cancelContext [out]

An optional pointer that receives a cancel context that can be passed to the <a href="https://msdn.microsoft.com/476a84c8-4065-4a4f-ad74-68cbbbabd5dd">CancelOperation</a>method to cancel an outstanding request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the request is submitted successfully (that is, calling this function doesn't immediately return an error), the result of the operation is available in the <a href="https://msdn.microsoft.com/5cc7bd36-3b8f-40af-badc-e8fc16d4a4c5">RequestCompletion</a> callback of the supplied <a href="https://msdn.microsoft.com/88746199-fc42-4f1d-9f97-ebd573e9cb3c">IDeviceRequestCompletionCallback</a> interface.

An operation that the system (operating system or device driver) fails immediately doesn't result in a callback.This means that the caller  receives a callback only if this function returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/d285e04e-04d0-4c2a-b9f0-72eebebf4f4b">IDeviceIoControl</a>
 

 

