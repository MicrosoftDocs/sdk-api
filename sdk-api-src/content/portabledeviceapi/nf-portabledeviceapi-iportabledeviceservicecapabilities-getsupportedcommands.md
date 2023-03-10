---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedCommands
title: IPortableDeviceServiceCapabilities::GetSupportedCommands (portabledeviceapi.h)
description: Retrieves the commands supported by the service.
helpviewer_keywords: ["GetSupportedCommands","GetSupportedCommands method [Windows Portable Devices SDK]","GetSupportedCommands method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedCommands method","IPortableDeviceServiceCapabilities.GetSupportedCommands","IPortableDeviceServiceCapabilities::GetSupportedCommands","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedCommands","wpdsdk.iportabledeviceservicecapabilities_getsupportedcommands"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedcommands.htm
tech.root: wpdsdk
ms.assetid: b116ae11-f02f-47aa-8c54-4810e2d50046
ms.date: 12/05/2018
ms.keywords: GetSupportedCommands, GetSupportedCommands method [Windows Portable Devices SDK], GetSupportedCommands method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedCommands method, IPortableDeviceServiceCapabilities.GetSupportedCommands, IPortableDeviceServiceCapabilities::GetSupportedCommands, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedCommands, wpdsdk.iportabledeviceservicecapabilities_getsupportedcommands
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
 - IPortableDeviceServiceCapabilities::GetSupportedCommands
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedCommands
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
 - IPortableDeviceServiceCapabilities.GetSupportedCommands
---

# IPortableDeviceServiceCapabilities::GetSupportedCommands


## -description

The <b>GetSupportedCommands</b> method retrieves the commands supported by the service.

## -parameters

### -param ppCommands [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that receives the list of commands.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>