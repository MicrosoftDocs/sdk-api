---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles
title: IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles (portabledeviceapi.h)
description: Retrieves the rendering profiles of a format.
helpviewer_keywords: ["GetFormatRenderingProfiles","GetFormatRenderingProfiles method [Windows Portable Devices SDK]","GetFormatRenderingProfiles method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetFormatRenderingProfiles method","IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles","IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles","portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles","wpdsdk.iportabledeviceservicecapabilities_getformatrenderingprofiles"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatrenderingprofiles.htm
tech.root: wpdsdk
ms.assetid: 38c9d357-17aa-4b26-9c01-c13a5cfcf495
ms.date: 12/05/2018
ms.keywords: GetFormatRenderingProfiles, GetFormatRenderingProfiles method [Windows Portable Devices SDK], GetFormatRenderingProfiles method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatRenderingProfiles method, IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles, IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles, wpdsdk.iportabledeviceservicecapabilities_getformatrenderingprofiles
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
 - IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles
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
 - IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles
---

# IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles


## -description

The <b>GetFormatRenderingProfiles</b> method retrieves the rendering profiles of a format.

## -parameters

### -param Format [in]

The format whose rendering profiles are retrieved.

### -param ppRenderingProfiles [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevaluescollection">IPortableDeviceValuesCollection</a> object that receives the list of rendering profiles.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

The rendering profiles are similar to what the <a href="/windows/desktop/wpd_sdk/wpd-functional-category-rendering-information">WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION</a> functional object returns for device-wide rendering profiles, so that the <b>DisplayRenderingProfile</b> helper function described in <a href="/windows/desktop/wpd_sdk/retrieving-the-rendering-capabilities-supported-by-a-device">Retrieving the Rendering Capabilities Supported by a Device</a> could be used here as well.    But there are differences: The <b>GetFormatRenderingProfiles</b> method retrieves only rendering profiles that apply to the selected service and have been filtered by format.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>