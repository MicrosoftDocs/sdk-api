---
UID: NF:portabledeviceapi.IPortableDeviceService.Methods
title: IPortableDeviceService::Methods (portabledeviceapi.h)
description: Retrieves the IPortableDeviceServiceMethods interface that is used to invoke custom functionality on the service.
helpviewer_keywords: ["IPortableDeviceService interface [Windows Portable Devices SDK]","Methods method","IPortableDeviceService.Methods","IPortableDeviceService::Methods","Methods","Methods method [Windows Portable Devices SDK]","Methods method [Windows Portable Devices SDK]","IPortableDeviceService interface","portabledeviceapi/IPortableDeviceService::Methods","wpdsdk.iportabledeviceservice_methods"]
old-location: wpdsdk\iportabledeviceservice_methods.htm
tech.root: wpdsdk
ms.assetid: 345102d4-3dac-4878-9196-bb0d97c0df07
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],Methods method, IPortableDeviceService.Methods, IPortableDeviceService::Methods, Methods, Methods method [Windows Portable Devices SDK], Methods method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::Methods, wpdsdk.iportabledeviceservice_methods
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
 - IPortableDeviceService::Methods
 - portabledeviceapi/IPortableDeviceService::Methods
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
 - IPortableDeviceService.Methods
---

# IPortableDeviceService::Methods


## -description

The <b>Methods</b> method retrieves the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods</a> interface that is used to invoke custom functionality on the service.

## -parameters

### -param ppMethods [out]

The <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods</a> interface used for invoking methods on the given service.

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



<a href="/windows/desktop/wpd_sdk/invoking-methods-synchronously">Invoking Service Methods</a>



<a href="/windows/desktop/wpd_sdk/invoking-methods-asynchronously">Invoking Service Methods Asynchronously</a>