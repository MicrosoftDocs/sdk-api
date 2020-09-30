---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetCommandOptions
title: IPortableDeviceServiceCapabilities::GetCommandOptions (portabledeviceapi.h)
description: Retrieves the options of a WPD command.
helpviewer_keywords: ["GetCommandOptions","GetCommandOptions method [Windows Portable Devices SDK]","GetCommandOptions method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetCommandOptions method","IPortableDeviceServiceCapabilities.GetCommandOptions","IPortableDeviceServiceCapabilities::GetCommandOptions","portabledeviceapi/IPortableDeviceServiceCapabilities::GetCommandOptions","wpdsdk.iportabledeviceservicecapabilities_getcommandoptions"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getcommandoptions.htm
tech.root: wpdsdk
ms.assetid: 5baa4c94-771a-430f-a963-800e4cd3a6b3
ms.date: 12/05/2018
ms.keywords: GetCommandOptions, GetCommandOptions method [Windows Portable Devices SDK], GetCommandOptions method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetCommandOptions method, IPortableDeviceServiceCapabilities.GetCommandOptions, IPortableDeviceServiceCapabilities::GetCommandOptions, portabledeviceapi/IPortableDeviceServiceCapabilities::GetCommandOptions, wpdsdk.iportabledeviceservicecapabilities_getcommandoptions
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
 - IPortableDeviceServiceCapabilities::GetCommandOptions
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetCommandOptions
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
 - IPortableDeviceServiceCapabilities.GetCommandOptions
---

# IPortableDeviceServiceCapabilities::GetCommandOptions


## -description

The <b>GetCommandOptions</b> method retrieves the options of a WPD command.

## -parameters

### -param Command [in]

The command whose options are retrieved.

### -param ppOptions [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of options.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>