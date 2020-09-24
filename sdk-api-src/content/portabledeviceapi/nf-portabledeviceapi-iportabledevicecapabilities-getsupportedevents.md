---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedEvents
title: IPortableDeviceCapabilities::GetSupportedEvents (portabledeviceapi.h)
description: The GetSupportedEvents method retrieves the supported events for this device.
helpviewer_keywords: ["GetSupportedEvents","GetSupportedEvents method [Windows Portable Devices SDK]","GetSupportedEvents method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetSupportedEvents method","IPortableDeviceCapabilities.GetSupportedEvents","IPortableDeviceCapabilities::GetSupportedEvents","IPortableDeviceCapabilitiesGetSupportedEvents","portabledeviceapi/IPortableDeviceCapabilities::GetSupportedEvents","wpdsdk.iportabledevicecapabilities_getsupportedevents"]
old-location: wpdsdk\iportabledevicecapabilities_getsupportedevents.htm
tech.root: wpdsdk
ms.assetid: f5082b2b-d925-4f9d-bbfd-edcf4553a6fa
ms.date: 12/05/2018
ms.keywords: GetSupportedEvents, GetSupportedEvents method [Windows Portable Devices SDK], GetSupportedEvents method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedEvents method, IPortableDeviceCapabilities.GetSupportedEvents, IPortableDeviceCapabilities::GetSupportedEvents, IPortableDeviceCapabilitiesGetSupportedEvents, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedEvents, wpdsdk.iportabledevicecapabilities_getsupportedevents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceCapabilities::GetSupportedEvents
 - portabledeviceapi/IPortableDeviceCapabilities::GetSupportedEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceCapabilities.GetSupportedEvents
---

# IPortableDeviceCapabilities::GetSupportedEvents


## -description

The <b>GetSupportedEvents</b> method retrieves the supported events for this device.

## -parameters

### -param ppEvents [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that lists the supported events. The caller must release this interface when it is done with it.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>