---
UID: NF:portabledeviceapi.IPortableDeviceService.Open
title: IPortableDeviceService::Open (portabledeviceapi.h)
description: Opens a connection to the service.
helpviewer_keywords: ["IPortableDeviceService interface [Windows Portable Devices SDK]","Open method","IPortableDeviceService.Open","IPortableDeviceService::Open","Open","Open method [Windows Portable Devices SDK]","Open method [Windows Portable Devices SDK]","IPortableDeviceService interface","portabledeviceapi/IPortableDeviceService::Open","wpdsdk.iportabledeviceservice_open"]
old-location: wpdsdk\iportabledeviceservice_open.htm
tech.root: wpdsdk
ms.assetid: 540d4320-42d4-48f0-8445-c74ff0dc1e1a
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],Open method, IPortableDeviceService.Open, IPortableDeviceService::Open, Open, Open method [Windows Portable Devices SDK], Open method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::Open, wpdsdk.iportabledeviceservice_open
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
 - IPortableDeviceService::Open
 - portabledeviceapi/IPortableDeviceService::Open
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
 - IPortableDeviceService.Open
---

# IPortableDeviceService::Open


## -description

The <b>Open</b> method opens a connection to the service.

## -parameters

### -param pszPnPServiceID [in]

The Plug and Play (PnP) identifier for the service, which is the same identifier that is retrieved by the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-getpnpserviceid">GetPnPServiceId</a> method.

### -param pClientInfo [in]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface specifying the client information.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The PnP identifier specified by the <i>pszPnPServiceID</i> parameter is invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_WPD_SERVICE_ALREADY_OPENED</b></dt>
</dl>
</td>
<td width="60%">
This method has already been called for the service.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>



<a href="/windows/desktop/wpd_sdk/opening-a-service">Opening a Service</a>