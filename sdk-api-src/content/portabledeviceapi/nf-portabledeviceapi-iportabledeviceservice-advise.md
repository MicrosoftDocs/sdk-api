---
UID: NF:portabledeviceapi.IPortableDeviceService.Advise
title: IPortableDeviceService::Advise (portabledeviceapi.h)
description: Registers an application-defined callback object that receives service events.
helpviewer_keywords: ["Advise","Advise method [Windows Portable Devices SDK]","Advise method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","Advise method","IPortableDeviceService.Advise","IPortableDeviceService::Advise","portabledeviceapi/IPortableDeviceService::Advise","wpdsdk.iportabledeviceservice_advise"]
old-location: wpdsdk\iportabledeviceservice_advise.htm
tech.root: wpdsdk
ms.assetid: 128b1ee9-fd1f-4480-ae9a-b1d0bc86cf1b
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Portable Devices SDK], Advise method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Advise method, IPortableDeviceService.Advise, IPortableDeviceService::Advise, portabledeviceapi/IPortableDeviceService::Advise, wpdsdk.iportabledeviceservice_advise
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
 - IPortableDeviceService::Advise
 - portabledeviceapi/IPortableDeviceService::Advise
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
 - IPortableDeviceService.Advise
---

# IPortableDeviceService::Advise


## -description

The <b>Advise</b> method registers an application-defined callback object that receives service events.

## -parameters

### -param dwFlags [in]

Not used.

### -param pCallback [in]

The  <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceeventcallback">IPortableDeviceEventCallback</a> interface specifying the callback object to register.

### -param pParameters [in]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface specifying the event-registration parameters, or <b>NULL</b> if the callback object is to receive all service events.

### -param ppszCookie [out]

The unique context ID for the callback object. This value matches that used by the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-unadvise">Unadvise</a> method to unregister the callback object.

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
A <b>NULL</b> value was specified for the <i>pCallback</i> parameter or the <i>ppszCookie</i> parameter.

</td>
</tr>
</table>

## -remarks

During cleanup, an application should unregister the callback object by calling the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-unadvise">Unadvise</a> method, and then release the memory referenced by the <i>ppszCookie</i> parameter by calling the <b>CoTaskMemFree</b> function.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>