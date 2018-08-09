---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatAttributes
title: IPortableDeviceServiceCapabilities::GetFormatAttributes
author: windows-sdk-content
description: Retrieves the attributes of a format.
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatattributes.htm
old-project: wpd_sdk
ms.assetid: 9fecc9e8-cc5c-4a5f-b5b4-71c63631948d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFormatAttributes, GetFormatAttributes method [Windows Portable Devices SDK], GetFormatAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatAttributes method, IPortableDeviceServiceCapabilities.GetFormatAttributes, IPortableDeviceServiceCapabilities::GetFormatAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatAttributes, wpdsdk.iportabledeviceservicecapabilities_getformatattributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IPortableDeviceServiceCapabilities.GetFormatAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceServiceCapabilities::GetFormatAttributes


## -description


The <b>GetFormatAttributes</b> method retrieves the attributes of a format.


## -parameters




### -param Format [in]

The format whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



<a href="https://msdn.microsoft.com/en-us/library/Dd389056(v=VS.85).aspx">WPD_FORMAT_ATTRIBUTE_NAME</a> is an example of a commonly retrieved attribute.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>
 

 

