---
UID: NN:portabledeviceapi.IPortableDevicePropertiesBulkCallback
title: IPortableDevicePropertiesBulkCallback (portabledeviceapi.h)
description: The IPortableDevicePropertiesBulkCallback interface is implemented by the application to track the progress of an asynchronous operation that was begun by using the IPortableDevicePropertiesBulk interface.After the application calls IPortableDevicePropertiesBulk::Start, Windows Portable Devices calls IPortableDevicePropertiesBulkCallback::OnStart first, and then repeatedly calls IPortableDevicePropertiesBulkCallback::OnProgress with information until the operation is completed or the application calls IPortableDevicePropertiesBulk::Cancel or returns an error value for OnProgress. Finally, regardless of whether the operation completed successfully, Windows Portable Devices calls IPortableDevicePropertiesBulkCallback::OnEnd.
helpviewer_keywords: ["IPortableDevicePropertiesBulkCallback","IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK]","IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK]","described","IPortableDevicePropertiesBulkCallbackInterface","portabledeviceapi/IPortableDevicePropertiesBulkCallback","wpdsdk.iportabledevicepropertiesbulkcallback"]
old-location: wpdsdk\iportabledevicepropertiesbulkcallback.htm
tech.root: wpdsdk
ms.assetid: 0a066e30-f584-4a8f-be08-c542060a335b
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulkCallback, IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK], IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesBulkCallbackInterface, portabledeviceapi/IPortableDevicePropertiesBulkCallback, wpdsdk.iportabledevicepropertiesbulkcallback
f1_keywords:
- portabledeviceapi/IPortableDevicePropertiesBulkCallback
dev_langs:
- c++
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
api_name:
- IPortableDevicePropertiesBulkCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDevicePropertiesBulkCallback interface


## -description



The <b>IPortableDevicePropertiesBulkCallback</b> interface is implemented by the application to track the progress of an asynchronous operation that was begun by using the <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk</a> interface.

After the application calls <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">IPortableDevicePropertiesBulk::Start</a>, Windows Portable Devices calls <b>IPortableDevicePropertiesBulkCallback::OnStart</b> first, and then repeatedly calls <b>IPortableDevicePropertiesBulkCallback::OnProgress</b> with information until the operation is completed or the application calls <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-cancel">IPortableDevicePropertiesBulk::Cancel</a> or returns an error value for <b>OnProgress</b>. Finally, regardless of whether the operation completed successfully, Windows Portable Devices calls <b>IPortableDevicePropertiesBulkCallback::OnEnd</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevicePropertiesBulkCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDevicePropertiesBulkCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulkcallback-onend">OnEnd</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulkcallback-onprogress">OnProgress</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> has sent data to the device and received some information back.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulkcallback-onstart">OnStart</a>
</td>
<td align="left" width="63%">
Called by the SDK when a bulk operation started by <b>IPortableDevicePropertiesBulk::Start</b> is about to begin.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 

