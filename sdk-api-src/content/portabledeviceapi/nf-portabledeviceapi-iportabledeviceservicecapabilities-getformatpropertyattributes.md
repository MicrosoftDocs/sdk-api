---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes
title: IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes (portabledeviceapi.h)
description: Retrieves the attributes of a format property.
helpviewer_keywords: ["GetFormatPropertyAttributes","GetFormatPropertyAttributes method [Windows Portable Devices SDK]","GetFormatPropertyAttributes method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetFormatPropertyAttributes method","IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes","IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes","portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes","wpdsdk.iportabledeviceservicecapabilities_getformatpropertyattributes"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatpropertyattributes.htm
tech.root: wpd_sdk
ms.assetid: a4120cfd-500d-47dd-87e9-418a32722332
ms.date: 12/05/2018
ms.keywords: GetFormatPropertyAttributes, GetFormatPropertyAttributes method [Windows Portable Devices SDK], GetFormatPropertyAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatPropertyAttributes method, IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes, IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes, wpdsdk.iportabledeviceservicecapabilities_getformatpropertyattributes
f1_keywords:
- portabledeviceapi/IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes
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
- IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes


## -description


The <b>GetFormatPropertyAttributes</b> method retrieves the attributes of a format property.


## -parameters




### -param Format [in]

The format whose property has its attributes retrieved.


### -param Property [in]

The property whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



A Windows Portable Devices (WPD) driver often treats objects of a given format the same. Many properties will therefore have attributes that are identical across all objects of that format. This method retrieves such attributes.

Note that this method will not retrieve attributes that differ across object instances.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>
 

 

