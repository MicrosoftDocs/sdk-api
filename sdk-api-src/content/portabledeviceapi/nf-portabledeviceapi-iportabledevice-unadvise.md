---
UID: NF:portabledeviceapi.IPortableDevice.Unadvise
title: IPortableDevice::Unadvise (portabledeviceapi.h)
description: The Unadvise method unregisters a client from receiving callback notifications. You must call this method if you called Advise previously.
helpviewer_keywords: ["IPortableDevice interface [Windows Portable Devices SDK]","Unadvise method","IPortableDevice.Unadvise","IPortableDevice::Unadvise","IPortableDeviceUnadvise","Unadvise","Unadvise method [Windows Portable Devices SDK]","Unadvise method [Windows Portable Devices SDK]","IPortableDevice interface","portabledeviceapi/IPortableDevice::Unadvise","wpdsdk.iportabledevice_unadvise"]
old-location: wpdsdk\iportabledevice_unadvise.htm
tech.root: wpdsdk
ms.assetid: 6720e92b-35cd-4e3f-bd21-36337cf80140
ms.date: 12/05/2018
ms.keywords: IPortableDevice interface [Windows Portable Devices SDK],Unadvise method, IPortableDevice.Unadvise, IPortableDevice::Unadvise, IPortableDeviceUnadvise, Unadvise, Unadvise method [Windows Portable Devices SDK], Unadvise method [Windows Portable Devices SDK],IPortableDevice interface, portabledeviceapi/IPortableDevice::Unadvise, wpdsdk.iportabledevice_unadvise
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
 - IPortableDevice::Unadvise
 - portabledeviceapi/IPortableDevice::Unadvise
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
 - IPortableDevice.Unadvise
---

# IPortableDevice::Unadvise


## -description

The <b>Unadvise</b> method unregisters a client from receiving callback notifications. You must call this method if you called <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-advise">Advise</a> previously.

## -parameters

### -param pszCookie [in]

Pointer to a null-terminated string that is a unique context ID. This was retrieved in the initial call to <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-advise">IPortableDevice::Advise</a>.

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
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>