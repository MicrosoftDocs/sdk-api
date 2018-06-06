---
UID: NF:d3d12.ID3D12Tools.EnableShaderInstrumentation
title: ID3D12Tools::EnableShaderInstrumentation
author: windows-sdk-content
description: This method enables tools such as PIX to instrument shaders.
old-location: direct3d12\id3d12tools_enableshaderinstrumentation.htm
old-project: direct3d12
ms.assetid: 35920253-1153-42AD-AEAC-2C646FF15879
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EnableShaderInstrumentation, EnableShaderInstrumentation method, EnableShaderInstrumentation method,ID3D12Tools interface, ID3D12Tools interface,EnableShaderInstrumentation method, ID3D12Tools.EnableShaderInstrumentation, ID3D12Tools::EnableShaderInstrumentation, d3d12/ID3D12Tools::EnableShaderInstrumentation, direct3d12.id3d12tools_enableshaderinstrumentation
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
 - ID3D12Tools.EnableShaderInstrumentation
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Tools::EnableShaderInstrumentation


## -description


This method enables tools such as PIX to instrument shaders.


## -parameters




### -param bEnable

Type: <b>BOOL</b>

TRUE to enable shader instrumentation; otherwise, FALSE.


## -returns



This method does not return a value.




## -remarks



Do not use this interface in your application, its not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.




## -see-also




<a href="https://msdn.microsoft.com/F192AC22-1FD9-496D-9943-99FB424DD214">ID3D12Tools</a>
 

 

