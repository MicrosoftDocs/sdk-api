---
UID: NF:d3d12.ID3D12Tools.ShaderInstrumentationEnabled
title: ID3D12Tools::ShaderInstrumentationEnabled
author: windows-sdk-content
description: Determines whether shader instrumentation is enabled.
old-location: direct3d12\id3d12tools_shaderinstrumentationenabled.htm
old-project: direct3d12
ms.assetid: 02A36358-5015-4CA1-B329-CCF074CF8F40
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12Tools interface,ShaderInstrumentationEnabled method, ID3D12Tools.ShaderInstrumentationEnabled, ID3D12Tools::ShaderInstrumentationEnabled, ShaderInstrumentationEnabled, ShaderInstrumentationEnabled method, ShaderInstrumentationEnabled method,ID3D12Tools interface, d3d12/ID3D12Tools::ShaderInstrumentationEnabled, direct3d12.id3d12tools_shaderinstrumentationenabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Tools.ShaderInstrumentationEnabled
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Tools::ShaderInstrumentationEnabled


## -description


Determines whether shader instrumentation is enabled.


## -parameters






## -returns



Type: <b>BOOL</b>

Returns TRUE if shader instrumentation is enabled; otherwise FALSE.




## -remarks



Do not use this interface in your application, its not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.




## -see-also




<a href="https://msdn.microsoft.com/F192AC22-1FD9-496D-9943-99FB424DD214">ID3D12Tools</a>
 

 

