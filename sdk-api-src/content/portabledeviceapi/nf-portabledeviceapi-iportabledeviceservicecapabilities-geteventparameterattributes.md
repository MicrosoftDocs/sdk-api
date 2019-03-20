---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetEventParameterAttributes
title: IPortableDeviceServiceCapabilities::GetEventParameterAttributes (portabledeviceapi.h)
author: windows-sdk-content
description: Retrieves the attributes of an event parameter.
old-location: wpdsdk\iportabledeviceservicecapabilities_geteventparameterattributes.htm
tech.root: wpd_sdk
ms.assetid: f842dc94-440f-4488-80e3-b10bf72e6269
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEventParameterAttributes, GetEventParameterAttributes method [Windows Portable Devices SDK], GetEventParameterAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetEventParameterAttributes method, IPortableDeviceServiceCapabilities.GetEventParameterAttributes, IPortableDeviceServiceCapabilities::GetEventParameterAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventParameterAttributes, wpdsdk.iportabledeviceservicecapabilities_geteventparameterattributes
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
 - IPortableDeviceServiceCapabilities.GetEventParameterAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceServiceCapabilities::GetEventParameterAttributes


## -description


The <b>GetEventParameterAttributes</b> method retrieves the attributes of an event parameter.


## -parameters




### -param Event

TBD


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that receives the list of attributes.


### -param Parameter [in]

The parameter whose attributes are retrieved.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Possible attribute values include the <a href="https://msdn.microsoft.com/en-us/library/Dd389006(v=VS.85).aspx">WPD_PARAMETER_ATTRIBUTE_VARTYPE</a> and WPD_PARAMETER_ATTRIBUTE_FORM properties.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>
 

 

