---
UID: NF:deviceaccess.IDeviceRequestCompletionCallback.RequestCompletion
title: IDeviceRequestCompletionCallback::RequestCompletion (deviceaccess.h)
description: Implement the RequestCompletion method to handle the completion of calls to the DeviceIoControlAsyncmethod.
old-location: deviceaccess\idevicerequestcompletioncallback_requestcompletion.htm
tech.root: deviceaccess
ms.assetid: 5cc7bd36-3b8f-40af-badc-e8fc16d4a4c5
ms.date: 12/05/2018
ms.keywords: IDeviceRequestCompletionCallback interface [Device Access Broker API],RequestCompletion method, IDeviceRequestCompletionCallback.RequestCompletion, IDeviceRequestCompletionCallback::RequestCompletion, RequestCompletion, RequestCompletion method [Device Access Broker API], RequestCompletion method [Device Access Broker API],IDeviceRequestCompletionCallback interface, deviceaccess.idevicerequestcompletioncallback_requestcompletion, deviceaccess/IDeviceRequestCompletionCallback::RequestCompletion
ms.topic: method
f1_keywords:
- deviceaccess/IDeviceRequestCompletionCallback.RequestCompletion
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- deviceaccess.h
api_name:
- IDeviceRequestCompletionCallback.RequestCompletion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceRequestCompletionCallback::RequestCompletion


## -description


Implement the <b>RequestCompletion</b> method to handle the completion of calls to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a>method. 


## -parameters




### -param requestResult [in]

The result code that's returned for the I/O operation.


### -param bytesReturned [in]

The number of bytes that were transferred as a result of the I/O operation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback">IDeviceRequestCompletionCallback</a>
 

 

