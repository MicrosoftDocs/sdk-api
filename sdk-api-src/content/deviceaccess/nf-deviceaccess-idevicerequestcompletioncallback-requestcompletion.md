---
UID: NF:deviceaccess.IDeviceRequestCompletionCallback.RequestCompletion
title: IDeviceRequestCompletionCallback::RequestCompletion method
author: windows-driver-content
description: Implement the RequestCompletion method to handle the completion of calls to the DeviceIoControlAsyncmethod.
old-location: deviceaccess\idevicerequestcompletioncallback_requestcompletion.htm
old-project: deviceaccess
ms.assetid: 5cc7bd36-3b8f-40af-badc-e8fc16d4a4c5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDeviceRequestCompletionCallback, IDeviceRequestCompletionCallback interface [Device Access Broker API], RequestCompletion method, IDeviceRequestCompletionCallback::RequestCompletion, RequestCompletion method [Device Access Broker API], RequestCompletion method [Device Access Broker API], IDeviceRequestCompletionCallback interface, RequestCompletion,IDeviceRequestCompletionCallback.RequestCompletion, deviceaccess.idevicerequestcompletioncallback_requestcompletion, deviceaccess/IDeviceRequestCompletionCallback::RequestCompletion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	deviceaccess.h
api_name:
-	IDeviceRequestCompletionCallback.RequestCompletion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDeviceRequestCompletionCallback::RequestCompletion method


## -description


Implement the <b>RequestCompletion</b> method to handle the completion of calls to the <a href="https://msdn.microsoft.com/550eadd0-c03b-40b3-9f08-639085365f4b">DeviceIoControlAsync</a>method. 


## -parameters




### -param requestResult [in]

The result code that's returned for the I/O operation.


### -param bytesReturned [in]

The number of bytes that were transferred as a result of the I/O operation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/88746199-fc42-4f1d-9f97-ebd573e9cb3c">IDeviceRequestCompletionCallback</a>
 

 

