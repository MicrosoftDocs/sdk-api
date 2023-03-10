---
UID: NN:deviceaccess.IDeviceRequestCompletionCallback
title: IDeviceRequestCompletionCallback (deviceaccess.h)
description: Provides a method to handle the completion of calls to the DeviceIoControlAsyncmethod.
helpviewer_keywords: ["IDeviceRequestCompletionCallback","IDeviceRequestCompletionCallback interface [Device Access Broker API]","IDeviceRequestCompletionCallback interface [Device Access Broker API]","described","deviceaccess.idevicerequestcompletioncallback","deviceaccess/IDeviceRequestCompletionCallback"]
old-location: deviceaccess\idevicerequestcompletioncallback.htm
tech.root: deviceaccess
ms.assetid: 88746199-fc42-4f1d-9f97-ebd573e9cb3c
ms.date: 12/05/2018
ms.keywords: IDeviceRequestCompletionCallback, IDeviceRequestCompletionCallback interface [Device Access Broker API], IDeviceRequestCompletionCallback interface [Device Access Broker API],described, deviceaccess.idevicerequestcompletioncallback, deviceaccess/IDeviceRequestCompletionCallback
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
 - IDeviceRequestCompletionCallback
 - deviceaccess/IDeviceRequestCompletionCallback
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
 - IDeviceRequestCompletionCallback
---

# IDeviceRequestCompletionCallback interface


## -description

Provides a method to handle the completion of calls to the <a href="/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a> method.

## -inheritance

The <b>IDeviceRequestCompletionCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceRequestCompletionCallback</b> also has these types of members:

## -remarks

Callers that want  to use asynchronous operations on an instance that's created by CreateDeviceAccessInstance should implement the <b>IDeviceRequestCompletionCallback</b> interface.
