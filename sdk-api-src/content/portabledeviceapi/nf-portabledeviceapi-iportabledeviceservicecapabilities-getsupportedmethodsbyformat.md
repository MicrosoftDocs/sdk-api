---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat
title: IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat (portabledeviceapi.h)
description: Retrieves the methods supported by the service for the specified format.helpviewer_keywords: ["GetSupportedMethodsByFormat","GetSupportedMethodsByFormat method [Windows Portable Devices SDK]","GetSupportedMethodsByFormat method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedMethodsByFormat method","IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat","IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat","wpdsdk.iportabledeviceservicecapabilities_getsupportedmethodsbyformat"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedmethodsbyformat.htm
tech.root: wpd_sdk
ms.assetid: f1950aa5-2316-4409-a7bd-1b87c6449187
ms.date: 12/05/2018
ms.keywords: GetSupportedMethodsByFormat, GetSupportedMethodsByFormat method [Windows Portable Devices SDK], GetSupportedMethodsByFormat method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedMethodsByFormat method, IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat, IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat, wpdsdk.iportabledeviceservicecapabilities_getsupportedmethodsbyformat
f1_keywords:
- portabledeviceapi/IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- PortableDeviceAPI.h
api_name:
- IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat


## -description


The <b>GetSupportedMethodsByFormat</b> method  retrieves the methods supported by the service for the specified format.


## -parameters




### -param Format [in]

The format whose supported methods are retrieved.


### -param ppMethods [out]

The <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that receives the list of methods.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>
 

 

