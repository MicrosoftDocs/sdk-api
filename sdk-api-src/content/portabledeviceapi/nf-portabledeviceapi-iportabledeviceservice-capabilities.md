---
UID: NF:portabledeviceapi.IPortableDeviceService.Capabilities
title: IPortableDeviceService::Capabilities (portabledeviceapi.h)
description: Retrieves the service capabilities.
helpviewer_keywords: ["Capabilities","Capabilities method [Windows Portable Devices SDK]","Capabilities method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","Capabilities method","IPortableDeviceService.Capabilities","IPortableDeviceService::Capabilities","portabledeviceapi/IPortableDeviceService::Capabilities","wpdsdk.iportabledeviceservice_capabilities"]
old-location: wpdsdk\iportabledeviceservice_capabilities.htm
tech.root: wpdsdk
ms.assetid: 62ef0c63-2908-458f-8e9f-eb6150441380
ms.date: 12/05/2018
ms.keywords: Capabilities, Capabilities method [Windows Portable Devices SDK], Capabilities method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Capabilities method, IPortableDeviceService.Capabilities, IPortableDeviceService::Capabilities, portabledeviceapi/IPortableDeviceService::Capabilities, wpdsdk.iportabledeviceservice_capabilities
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceService::Capabilities
 - portabledeviceapi/IPortableDeviceService::Capabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.Capabilities
---

# IPortableDeviceService::Capabilities


## -description

The <b>Capabilities</b> method retrieves the service capabilities.

## -parameters

### -param ppCapabilities [out]

The <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities</a> interface specifying the capabilities of the service.

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
A <b>NULL</b> parameter was specified.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-events">Retrieving Supported Service Events</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-formats">Retrieving Supported Service Formats</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>