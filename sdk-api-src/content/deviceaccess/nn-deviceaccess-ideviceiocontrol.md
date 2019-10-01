---
UID: NN:deviceaccess.IDeviceIoControl
title: IDeviceIoControl (deviceaccess.h)
author: windows-sdk-content
description: Sends a control code to a device driver.This action causes the device to perform the corresponding operation.
old-location: deviceaccess\ideviceiocontrol.htm
tech.root: deviceaccess
ms.assetid: d285e04e-04d0-4c2a-b9f0-72eebebf4f4b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDeviceIoControl, IDeviceIoControl interface [Device Access Broker API], IDeviceIoControl interface [Device Access Broker API],described, deviceaccess.ideviceiocontrol, deviceaccess/IDeviceIoControl
ms.topic: interface
f1_keywords: 
 - "deviceaccess/IDeviceIoControl"
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
 - IDeviceIoControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceIoControl interface


## -description


Sends a control code to a device driver.This action causes the device to perform the corresponding operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceIoControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceIoControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeviceIoControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-canceloperation">CancelOperation</a>
</td>
<td align="left" width="63%">
Attempts to cancel a previously issued call by using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync">DeviceIoControlAsync</a>
</td>
<td align="left" width="63%">
Sends an asynchronous device I/O control request to the device interface that's specified by the call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolsync">DeviceIoControlSync</a>
</td>
<td align="left" width="63%">
Sends a synchronous device I/O control request to the device interface that's specified by the call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance">CreateDeviceAccessInstance</a>.

</td>
</tr>
</table> 

