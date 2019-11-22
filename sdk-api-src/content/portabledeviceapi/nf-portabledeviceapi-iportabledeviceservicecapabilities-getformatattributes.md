---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatAttributes
title: IPortableDeviceServiceCapabilities::GetFormatAttributes (portabledeviceapi.h)

description: Retrieves the attributes of a format.
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatattributes.htm
tech.root: wpd_sdk
ms.assetid: 9fecc9e8-cc5c-4a5f-b5b4-71c63631948d

ms.date: 12/05/2018
ms.keywords: GetFormatAttributes, GetFormatAttributes method [Windows Portable Devices SDK], GetFormatAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatAttributes method, IPortableDeviceServiceCapabilities.GetFormatAttributes, IPortableDeviceServiceCapabilities::GetFormatAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatAttributes, wpdsdk.iportabledeviceservicecapabilities_getformatattributes
ms.topic: method
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceServiceCapabilities.GetFormatAttributes"
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
 - IPortableDeviceServiceCapabilities.GetFormatAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceCapabilities::GetFormatAttributes


## -description


The <b>GetFormatAttributes</b> method retrieves the attributes of a format.


## -parameters




### -param Format [in]

The format whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/wpd-format-attributes">WPD_FORMAT_ATTRIBUTE_NAME</a> is an example of a commonly retrieved attribute.
      


#### Examples

For an example of how to use this method, see <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/retrieving-supported-formats">Retrieving Supported Service Formats</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/retrieving-supported-formats">Retrieving Supported Service Formats</a>
 

 

