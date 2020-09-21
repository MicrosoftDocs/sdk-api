---
UID: NF:portabledeviceapi.IPortableDeviceService.GetPnPServiceID
title: IPortableDeviceService::GetPnPServiceID (portabledeviceapi.h)
description: Retrieves a Plug and Play (PnP) identifier for the service.
helpviewer_keywords: ["GetPnPServiceID","GetPnPServiceID method [Windows Portable Devices SDK]","GetPnPServiceID method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","GetPnPServiceID method","IPortableDeviceService.GetPnPServiceID","IPortableDeviceService::GetPnPServiceID","portabledeviceapi/IPortableDeviceService::GetPnPServiceID","wpdsdk.iportabledeviceservice_getpnpserviceid"]
old-location: wpdsdk\iportabledeviceservice_getpnpserviceid.htm
tech.root: wpdsdk
ms.assetid: c73261a5-1436-4706-8d8b-ff8183429ac4
ms.date: 12/05/2018
ms.keywords: GetPnPServiceID, GetPnPServiceID method [Windows Portable Devices SDK], GetPnPServiceID method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],GetPnPServiceID method, IPortableDeviceService.GetPnPServiceID, IPortableDeviceService::GetPnPServiceID, portabledeviceapi/IPortableDeviceService::GetPnPServiceID, wpdsdk.iportabledeviceservice_getpnpserviceid
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
 - IPortableDeviceService::GetPnPServiceID
 - portabledeviceapi/IPortableDeviceService::GetPnPServiceID
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
 - IPortableDeviceService.GetPnPServiceID
---

# IPortableDeviceService::GetPnPServiceID


## -description

The <b>GetPnPServiceID</b> method retrieves a Plug and Play (PnP) identifier for the service.

## -parameters

### -param ppszPnPServiceID [out]

The retrieved PnP identifier, which is the same identifier that was passed to the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-open">Open</a> method.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_WPD_SERVICE_NOT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-open">Open</a> method has not yet been called for the service.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-open">Open</a> method must be called on the service before a PnP identifier can be retrieved.

When an application no longer needs the PnP identifier, it should call the <b>CoTaskMemFree</b> function to free the identifier memory.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>