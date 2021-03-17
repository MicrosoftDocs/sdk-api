---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetMethodParameterAttributes
title: IPortableDeviceServiceCapabilities::GetMethodParameterAttributes (portabledeviceapi.h)
description: Retrieves the attributes used to describe a given method parameter.
helpviewer_keywords: ["GetMethodParameterAttributes","GetMethodParameterAttributes method [Windows Portable Devices SDK]","GetMethodParameterAttributes method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetMethodParameterAttributes method","IPortableDeviceServiceCapabilities.GetMethodParameterAttributes","IPortableDeviceServiceCapabilities::GetMethodParameterAttributes","portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodParameterAttributes","wpdsdk.iportabledeviceservicecapabilities_getmethodparameterattributes"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getmethodparameterattributes.htm
tech.root: wpdsdk
ms.assetid: 48c566e1-981f-4173-ad5b-a7b1b7c35d06
ms.date: 12/05/2018
ms.keywords: GetMethodParameterAttributes, GetMethodParameterAttributes method [Windows Portable Devices SDK], GetMethodParameterAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetMethodParameterAttributes method, IPortableDeviceServiceCapabilities.GetMethodParameterAttributes, IPortableDeviceServiceCapabilities::GetMethodParameterAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodParameterAttributes, wpdsdk.iportabledeviceservicecapabilities_getmethodparameterattributes
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
 - IPortableDeviceServiceCapabilities::GetMethodParameterAttributes
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodParameterAttributes
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
 - IPortableDeviceServiceCapabilities.GetMethodParameterAttributes
---

# IPortableDeviceServiceCapabilities::GetMethodParameterAttributes


## -description

The <b>GetMethodParameterAttributes</b> method retrieves the attributes used to describe a given method parameter.

## -parameters

### -param Method

The method that contains the parameter whose attributes are retrieved.

### -param ppAttributes [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.

### -param Parameter [in]

The parameter whose attributes are retrieved.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

Possible attributes include the <a href="/windows/desktop/wpd_sdk/wpd-attributes">WPD_PARAMETER_ATTRIBUTE_ORDER</a>, <b>WPD_PARAMETER_ATTRIBUTE_USAGE</b>, <b>WPD_PARAMETER_ATTRIBUTE_NAME</b>, and <b>WPD_PARAMETER_ATTRIBUTE_VARTYPE</b> properties.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>