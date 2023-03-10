---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetEventOptions
title: IPortableDeviceCapabilities::GetEventOptions (portabledeviceapi.h)
description: The GetEventOptions method retrieves all the supported options for the specified event on the device.
helpviewer_keywords: ["GetEventOptions","GetEventOptions method [Windows Portable Devices SDK]","GetEventOptions method [Windows Portable Devices SDK]","IPortableDeviceCapabilities method","IPortableDeviceCapabilities method [Windows Portable Devices SDK]","GetEventOptions method","IPortableDeviceCapabilities.GetEventOptions","IPortableDeviceCapabilities::GetEventOptions","IPortableDeviceCapabilitiesGetEventOptions","portabledeviceapi/IPortableDeviceCapabilities::GetEventOptions","wpdsdk.iportabledevicecapabilities_geteventoptions"]
old-location: wpdsdk\iportabledevicecapabilities_geteventoptions.htm
tech.root: wpdsdk
ms.assetid: b4d3495b-b2d3-4d0d-8dc6-df030a52ab3f
ms.date: 12/05/2018
ms.keywords: GetEventOptions, GetEventOptions method [Windows Portable Devices SDK], GetEventOptions method [Windows Portable Devices SDK],IPortableDeviceCapabilities method, IPortableDeviceCapabilities method [Windows Portable Devices SDK],GetEventOptions method, IPortableDeviceCapabilities.GetEventOptions, IPortableDeviceCapabilities::GetEventOptions, IPortableDeviceCapabilitiesGetEventOptions, portabledeviceapi/IPortableDeviceCapabilities::GetEventOptions, wpdsdk.iportabledevicecapabilities_geteventoptions
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
 - IPortableDeviceCapabilities::GetEventOptions
 - portabledeviceapi/IPortableDeviceCapabilities::GetEventOptions
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
 - IPortableDeviceCapabilities.GetEventOptions
---

# IPortableDeviceCapabilities::GetEventOptions


## -description

The <b>GetEventOptions</b> method retrieves all the supported options for the specified event on the device.

## -parameters

### -param Event [in]

A <b>REFGUID</b> that specifies a event to query for supported options. For a list of the events that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/commands">Events</a>.

### -param ppOptions [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the supported options. If no options are supported, this will not contain any values. The caller must release this interface when it is done with it.

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

<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-geteventoptions">IPortableDeviceCapabilities</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>