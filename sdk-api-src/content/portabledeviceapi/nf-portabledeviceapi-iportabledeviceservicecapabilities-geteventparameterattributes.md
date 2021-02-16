---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetEventParameterAttributes
title: IPortableDeviceServiceCapabilities::GetEventParameterAttributes (portabledeviceapi.h)
description: Retrieves the attributes of an event parameter.
helpviewer_keywords: ["GetEventParameterAttributes","GetEventParameterAttributes method [Windows Portable Devices SDK]","GetEventParameterAttributes method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetEventParameterAttributes method","IPortableDeviceServiceCapabilities.GetEventParameterAttributes","IPortableDeviceServiceCapabilities::GetEventParameterAttributes","portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventParameterAttributes","wpdsdk.iportabledeviceservicecapabilities_geteventparameterattributes"]
old-location: wpdsdk\iportabledeviceservicecapabilities_geteventparameterattributes.htm
tech.root: wpdsdk
ms.assetid: f842dc94-440f-4488-80e3-b10bf72e6269
ms.date: 12/05/2018
ms.keywords: GetEventParameterAttributes, GetEventParameterAttributes method [Windows Portable Devices SDK], GetEventParameterAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetEventParameterAttributes method, IPortableDeviceServiceCapabilities.GetEventParameterAttributes, IPortableDeviceServiceCapabilities::GetEventParameterAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventParameterAttributes, wpdsdk.iportabledeviceservicecapabilities_geteventparameterattributes
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
 - IPortableDeviceServiceCapabilities::GetEventParameterAttributes
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventParameterAttributes
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
 - IPortableDeviceServiceCapabilities.GetEventParameterAttributes
---

# IPortableDeviceServiceCapabilities::GetEventParameterAttributes


## -description

The <b>GetEventParameterAttributes</b> method retrieves the attributes of an event parameter.

## -parameters

### -param Event

The event that contains the parameter whose attributes are retrieved.

### -param ppAttributes [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.

### -param Parameter [in]

The parameter whose attributes are retrieved.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

Possible attribute values include the <a href="/windows/desktop/wpd_sdk/wpd-attributes">WPD_PARAMETER_ATTRIBUTE_VARTYPE</a> and WPD_PARAMETER_ATTRIBUTE_FORM properties.


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/retrieving-supported-events">Retrieving Supported Service Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-events">Retrieving Supported Service Events</a>