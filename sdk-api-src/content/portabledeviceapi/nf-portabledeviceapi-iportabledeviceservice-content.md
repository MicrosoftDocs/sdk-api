---
UID: NF:portabledeviceapi.IPortableDeviceService.Content
title: IPortableDeviceService::Content (portabledeviceapi.h)
description: Retrieves access to the service content.
helpviewer_keywords: ["Content","Content method [Windows Portable Devices SDK]","Content method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","Content method","IPortableDeviceService.Content","IPortableDeviceService::Content","portabledeviceapi/IPortableDeviceService::Content","wpdsdk.iportabledeviceservice_content"]
old-location: wpdsdk\iportabledeviceservice_content.htm
tech.root: wpdsdk
ms.assetid: 36977b23-b03f-48bc-8313-ddfe2ef208de
ms.date: 12/05/2018
ms.keywords: Content, Content method [Windows Portable Devices SDK], Content method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Content method, IPortableDeviceService.Content, IPortableDeviceService::Content, portabledeviceapi/IPortableDeviceService::Content, wpdsdk.iportabledeviceservice_content
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
 - IPortableDeviceService::Content
 - portabledeviceapi/IPortableDeviceService::Content
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
 - IPortableDeviceService.Content
---

# IPortableDeviceService::Content


## -description

The <b>Content</b> method retrieves access to the service content.

## -parameters

### -param ppContent [out]

The <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent2">IPortableDeviceContent2</a> interface that accesses the service content.

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

<a href="/windows/desktop/wpd_sdk/enumerating-service-content">Enumerating Service Content</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-content-object-properties">Retrieving Content-Object Properties</a>



<a href="/windows/desktop/wpd_sdk/writing-content-object-properties">Writing Content-Object Properties</a>