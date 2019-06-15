---
UID: NN:deviceaccess.IDeviceRequestCompletionCallback
title: IDeviceRequestCompletionCallback (deviceaccess.h)
author: windows-sdk-content
description: Provides a method to handle the completion of calls to the DeviceIoControlAsyncmethod.
old-location: deviceaccess\idevicerequestcompletioncallback.htm
tech.root: deviceaccess
ms.assetid: 88746199-fc42-4f1d-9f97-ebd573e9cb3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDeviceRequestCompletionCallback, IDeviceRequestCompletionCallback interface [Device Access Broker API], IDeviceRequestCompletionCallback interface [Device Access Broker API],described, deviceaccess.idevicerequestcompletioncallback, deviceaccess/IDeviceRequestCompletionCallback
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceRequestCompletionCallback interface


## -description


Provides a method to handle the completion of calls to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a>method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceRequestCompletionCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceRequestCompletionCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeviceRequestCompletionCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-idevicerequestcompletioncallback-requestcompletion">RequestCompletion</a>
</td>
<td align="left" width="63%">
Implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-idevicerequestcompletioncallback-requestcompletion">RequestCompletion</a> method to handle the completion of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a> calls. 

</td>
</tr>
</table> 


## -remarks



Callers that want  to use asynchronous operations on an instance that's created by CreateDeviceAccessInstance should implement the <b>IDeviceRequestCompletionCallback</b> interface.



