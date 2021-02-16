---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedFormatProperties
title: IPortableDeviceServiceCapabilities::GetSupportedFormatProperties (portabledeviceapi.h)
description: Retrieves the properties supported by the service for the specified format.
helpviewer_keywords: ["GetSupportedFormatProperties","GetSupportedFormatProperties method [Windows Portable Devices SDK]","GetSupportedFormatProperties method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedFormatProperties method","IPortableDeviceServiceCapabilities.GetSupportedFormatProperties","IPortableDeviceServiceCapabilities::GetSupportedFormatProperties","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormatProperties","wpdsdk.iportabledeviceservicecapabilities_getsupportedformatproperties"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedformatproperties.htm
tech.root: wpdsdk
ms.assetid: 80ce7975-c567-4c99-9eb5-6d494a0f1883
ms.date: 12/05/2018
ms.keywords: GetSupportedFormatProperties, GetSupportedFormatProperties method [Windows Portable Devices SDK], GetSupportedFormatProperties method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedFormatProperties method, IPortableDeviceServiceCapabilities.GetSupportedFormatProperties, IPortableDeviceServiceCapabilities::GetSupportedFormatProperties, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormatProperties, wpdsdk.iportabledeviceservicecapabilities_getsupportedformatproperties
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceapi.idl
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
 - IPortableDeviceServiceCapabilities::GetSupportedFormatProperties
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedFormatProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceServiceCapabilities.GetSupportedFormatProperties
---

# IPortableDeviceServiceCapabilities::GetSupportedFormatProperties


## -description

The <b>GetSupportedFormatProperties</b> method retrieves the properties supported by the service for the specified format.

## -parameters

### -param Format [in]

The format whose properties are retrieved.

### -param ppKeys [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that receives the list of properties.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

The retrieved property collection is a superset of all properties supported by an object of the specified format.

An application can also retrieve the properties for an object by calling the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservice-sendcommand">IPortableDeviceService::SendCommand</a> method with the <a href="/windows/desktop/wpd_sdk/wpd-command-object-properties-get-supported2">WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED</a> property passed as the command identifier. However, the <b>GetSupportedFormatProperties</b> method is typically faster than the <b>IPortableDeviceService::SendCommand</b> method.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>