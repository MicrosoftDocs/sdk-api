---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetMethodAttributes
title: IPortableDeviceServiceCapabilities::GetMethodAttributes (portabledeviceapi.h)
description: Retrieves the attributes used to describe a given method.
helpviewer_keywords: ["GetMethodAttributes","GetMethodAttributes method [Windows Portable Devices SDK]","GetMethodAttributes method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetMethodAttributes method","IPortableDeviceServiceCapabilities.GetMethodAttributes","IPortableDeviceServiceCapabilities::GetMethodAttributes","portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodAttributes","wpdsdk.iportabledeviceservicecapabilities_getmethodattributes"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getmethodattributes.htm
tech.root: wpdsdk
ms.assetid: 4cd125ea-545f-461b-90e1-88d3e3a6c032
ms.date: 12/05/2018
ms.keywords: GetMethodAttributes, GetMethodAttributes method [Windows Portable Devices SDK], GetMethodAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetMethodAttributes method, IPortableDeviceServiceCapabilities.GetMethodAttributes, IPortableDeviceServiceCapabilities::GetMethodAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodAttributes, wpdsdk.iportabledeviceservicecapabilities_getmethodattributes
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
 - IPortableDeviceServiceCapabilities::GetMethodAttributes
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetMethodAttributes
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
 - IPortableDeviceServiceCapabilities.GetMethodAttributes
---

# IPortableDeviceServiceCapabilities::GetMethodAttributes


## -description

The <b>GetMethodAttributes</b> method retrieves the attributes used to describe a given method.

## -parameters

### -param Method [in]

The method whose attributes are retrieved.

### -param ppAttributes [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

Possible attributes include the <a href="/windows/desktop/wpd_sdk/wpd-attributes">WPD_METHOD_ATTRIBUTE_NAME</a>, <b>WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT</b>, <b>WPD_METHOD_ATTRIBUTE_ACCESS</b>, and <a href="/windows/desktop/wpd_sdk/wpd-method-attributes">WPD_METHOD_ATTRIBUTE_PARAMETERS</a> properties.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/wpd_sdk/device-interface-guids">Device Interface GUIDs</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="/windows/desktop/wpd_sdk/wpd-attributes">Method, Format, and Parameter Attributes</a>



<a href="/windows/desktop/wpd_sdk/retrieving-supported-methods">Retrieving Supported Service Methods</a>