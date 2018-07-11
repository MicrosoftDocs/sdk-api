---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes
title: IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes
author: windows-sdk-content
description: Retrieves the attributes of a format property.
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatpropertyattributes.htm
old-project: wpd_sdk
ms.assetid: a4120cfd-500d-47dd-87e9-418a32722332
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: GetFormatPropertyAttributes, GetFormatPropertyAttributes method [Windows Portable Devices SDK], GetFormatPropertyAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatPropertyAttributes method, IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes, IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes, wpdsdk.iportabledeviceservicecapabilities_getformatpropertyattributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetFormatPropertyAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



A Windows Portable Devices (WPD) driver often treats objects of a given format the same. Many properties will therefore have attributes that are identical across all objects of that format. This method retrieves such attributes.

Note that this method will not retrieve attributes that differ across object instances.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

