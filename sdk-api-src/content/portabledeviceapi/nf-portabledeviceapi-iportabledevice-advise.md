---
UID: NF:portabledeviceapi.IPortableDevice.Advise
title: IPortableDevice::Advise (portabledeviceapi.h)
description: The Advise method registers an application-defined callback that receives device events.
helpviewer_keywords: ["Advise","Advise method [Windows Portable Devices SDK]","Advise method [Windows Portable Devices SDK]","IPortableDevice interface","IPortableDevice interface [Windows Portable Devices SDK]","Advise method","IPortableDevice.Advise","IPortableDevice::Advise","IPortableDeviceAdvise","portabledeviceapi/IPortableDevice::Advise","wpdsdk.iportabledevice_advise"]
old-location: wpdsdk\iportabledevice_advise.htm
tech.root: wpdsdk
ms.assetid: bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Portable Devices SDK], Advise method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Advise method, IPortableDevice.Advise, IPortableDevice::Advise, IPortableDeviceAdvise, portabledeviceapi/IPortableDevice::Advise, wpdsdk.iportabledevice_advise
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
 - IPortableDevice::Advise
 - portabledeviceapi/IPortableDevice::Advise
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
 - IPortableDevice.Advise
---

# IPortableDevice::Advise


## -description

The <b>Advise</b> method registers an application-defined callback that receives device events.

## -parameters

### -param dwFlags [in]

<b>DWORD</b> that specifies option flags.

### -param pCallback [in]

Pointer to a callback object.

### -param pParameters [in]

This parameter is ignored and should be set to <b>NULL</b>.

### -param ppszCookie [out]

A string that represents a unique context ID. This is used to unregister for callbacks when calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-unadvise">Unadvise</a>.

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
The application-defined callback was successfully registered.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wpd_sdk/handling-events-from-the-device">Handling Events from the Device</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>