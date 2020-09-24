---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedFormats
title: IPortableDeviceServiceCapabilities::GetSupportedFormats (portabledeviceapi.h)
description: Retrieves the formats supported by the service.
helpviewer_keywords: ["GetSupportedFormats","GetSupportedFormats method [Windows Portable Devices SDK]","GetSupportedFormats method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedFormats method","IPortableDeviceServiceCapabilities.GetSupportedFormats","IPortableDeviceServiceCapabilities::GetSupportedFormats","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormats","wpdsdk.iportabledeviceservicecapabilities_getsupportedformats"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedformats.htm
tech.root: wpdsdk
ms.assetid: 1df1ed1b-d231-4327-84eb-1bcf74dd881b
ms.date: 12/05/2018
ms.keywords: GetSupportedFormats, GetSupportedFormats method [Windows Portable Devices SDK], GetSupportedFormats method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedFormats method, IPortableDeviceServiceCapabilities.GetSupportedFormats, IPortableDeviceServiceCapabilities::GetSupportedFormats, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormats, wpdsdk.iportabledeviceservicecapabilities_getsupportedformats
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
 - IPortableDeviceServiceCapabilities::GetSupportedFormats
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormats
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
 - IPortableDeviceServiceCapabilities.GetSupportedFormats
---

# IPortableDeviceServiceCapabilities::GetSupportedFormats


## -description

The <b>GetSupportedFormats</b> method retrieves the formats supported by the  service.

## -parameters

### -param ppFormats [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that receives the list of formats.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-formats">Retrieving Supported Service Formats</a>