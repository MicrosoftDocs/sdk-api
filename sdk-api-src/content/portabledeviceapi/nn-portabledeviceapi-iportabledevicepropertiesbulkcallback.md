---
UID: NN:portabledeviceapi.IPortableDevicePropertiesBulkCallback
title: IPortableDevicePropertiesBulkCallback
author: windows-sdk-content
description: The IPortableDevicePropertiesBulkCallback interface is implemented by the application to track the progress of an asynchronous operation that was begun by using the IPortableDevicePropertiesBulk interface.After the application calls IPortableDevicePropertiesBulk::Start, Windows Portable Devices calls IPortableDevicePropertiesBulkCallback::OnStart first, and then repeatedly calls IPortableDevicePropertiesBulkCallback::OnProgress with information until the operation is completed or the application calls IPortableDevicePropertiesBulk::Cancel or returns an error value for OnProgress. Finally, regardless of whether the operation completed successfully, Windows Portable Devices calls IPortableDevicePropertiesBulkCallback::OnEnd.
old-location: wpdsdk\iportabledevicepropertiesbulkcallback.htm
old-project: wpd_sdk
ms.assetid: 0a066e30-f584-4a8f-be08-c542060a335b
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDevicePropertiesBulkCallback, IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK], IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesBulkCallbackInterface, portabledeviceapi/IPortableDevicePropertiesBulkCallback, wpdsdk.iportabledevicepropertiesbulkcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevicePropertiesBulkCallback
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDevicePropertiesBulkCallback interface


## -description



The <b>IPortableDevicePropertiesBulkCallback</b> interface is implemented by the application to track the progress of an asynchronous operation that was begun by using the <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk</a> interface.

After the application calls <a href="https://msdn.microsoft.com/a69afdc9-622d-45fc-b71e-6058d9d528b0">IPortableDevicePropertiesBulk::Start</a>, Windows Portable Devices calls <b>IPortableDevicePropertiesBulkCallback::OnStart</b> first, and then repeatedly calls <b>IPortableDevicePropertiesBulkCallback::OnProgress</b> with information until the operation is completed or the application calls <a href="https://msdn.microsoft.com/18a3458d-df93-4bdf-b5f2-f0197c35a1dd">IPortableDevicePropertiesBulk::Cancel</a> or returns an error value for <b>OnProgress</b>. Finally, regardless of whether the operation completed successfully, Windows Portable Devices calls <b>IPortableDevicePropertiesBulkCallback::OnEnd</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevicePropertiesBulkCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDevicePropertiesBulkCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDevicePropertiesBulkCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926906">OnEnd</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f357d7da-00cd-4439-af6d-5d3716a8443b">OnProgress</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> has sent data to the device and received some information back.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bde04e04-d36e-4471-b598-ee38dba9f614">OnStart</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> is about to begin.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

