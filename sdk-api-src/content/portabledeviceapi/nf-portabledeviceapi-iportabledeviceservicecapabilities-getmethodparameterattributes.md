---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetMethodParameterAttributes
title: IPortableDeviceServiceCapabilities::GetMethodParameterAttributes
author: windows-sdk-content
description: Retrieves the attributes used to describe a given method parameter.
old-location: wpdsdk\iportabledeviceservicecapabilities_getmethodparameterattributes.htm
tech.root: wpd_sdk
ms.assetid: 48c566e1-981f-4173-ad5b-a7b1b7c35d06
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMethodParameterAttributes, GetMethodParameterAttributes method [Windows Portable Devices SDK], GetMethodParameterAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetMethodParameterAttributes method, IPortableDeviceServiceCapabilities.GetMethodParameterAttributes, IPortableDeviceServiceCapabilities::GetMethodParameterAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodParameterAttributes, wpdsdk.iportabledeviceservicecapabilities_getmethodparameterattributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPortableDeviceServiceCapabilities.GetMethodParameterAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- portabledeviceapi.h
: 
- IPortableDeviceServiceCapabilities.GetMethodParameterAttributes
: 
---

# IPortableDeviceServiceCapabilities::GetMethodParameterAttributes


## -description


The <b>GetMethodParameterAttributes</b> method retrieves the attributes used to describe a given method parameter.


## -parameters




### -param Method

TBD


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that receives the list of attributes.


### -param Parameter [in]

The parameter whose attributes are retrieved.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Possible attributes include the <a href="wpd_attributes.htm">WPD_PARAMETER_ATTRIBUTE_ORDER</a>, <b>WPD_PARAMETER_ATTRIBUTE_USAGE</b>, <b>WPD_PARAMETER_ATTRIBUTE_NAME</b>, and <b>WPD_PARAMETER_ATTRIBUTE_VARTYPE</b> properties.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

