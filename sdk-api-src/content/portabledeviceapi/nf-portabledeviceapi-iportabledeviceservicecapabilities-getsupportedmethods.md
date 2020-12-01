---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedMethods
title: IPortableDeviceServiceCapabilities::GetSupportedMethods (portabledeviceapi.h)
description: Retrieves the methods supported by the service.
helpviewer_keywords: ["GetSupportedMethods","GetSupportedMethods method [Windows Portable Devices SDK]","GetSupportedMethods method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedMethods method","IPortableDeviceServiceCapabilities.GetSupportedMethods","IPortableDeviceServiceCapabilities::GetSupportedMethods","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethods","wpdsdk.iportabledeviceservicecapabilities_getsupportedmethods"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedmethods.htm
tech.root: wpdsdk
ms.assetid: 60201d12-5a49-4d84-9dae-b04cbb144d8f
ms.date: 12/05/2018
ms.keywords: GetSupportedMethods, GetSupportedMethods method [Windows Portable Devices SDK], GetSupportedMethods method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedMethods method, IPortableDeviceServiceCapabilities.GetSupportedMethods, IPortableDeviceServiceCapabilities::GetSupportedMethods, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethods, wpdsdk.iportabledeviceservicecapabilities_getsupportedmethods
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
 - IPortableDeviceServiceCapabilities::GetSupportedMethods
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethods
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
 - IPortableDeviceServiceCapabilities.GetSupportedMethods
---

# IPortableDeviceServiceCapabilities::GetSupportedMethods


## -description

The <b>GetSupportedMethods</b> method retrieves the methods supported by the service.

## -parameters

### -param ppMethods [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that receives the list of methods.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>