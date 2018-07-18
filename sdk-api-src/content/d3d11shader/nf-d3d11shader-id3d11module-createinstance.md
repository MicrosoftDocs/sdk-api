---
UID: NF:d3d11shader.ID3D11Module.CreateInstance
title: ID3D11Module::CreateInstance
author: windows-sdk-content
description: Initializes an instance of a shader module that is used for resource rebinding.
old-location: direct3d11\id3d11module_createinstance.htm
old-project: direct3d11
ms.assetid: 737A69EF-F74E-4480-98EA-31D6CCAC0F8A
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: CreateInstance, CreateInstance method [Direct3D 11], CreateInstance method [Direct3D 11],ID3D11Module interface, ID3D11Module interface [Direct3D 11],CreateInstance method, ID3D11Module.CreateInstance, ID3D11Module::CreateInstance, d3d11shader/ID3D11Module::CreateInstance, direct3d11.id3d11module_createinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11shader.h
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11Module.CreateInstance
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11Module::CreateInstance


## -description


Initializes an instance of a shader module that is used for resource rebinding.


## -parameters




### -param pNamespace [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of a shader module to initialize. This can be <b>NULL</b> if you don't want to specify a name for the module.


### -param ppModuleInstance [out]

Type: <b><a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a> interface to initialize.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5915DACB-1D3A-496C-96C6-77D85CC6560B">ID3D11Module</a>
 

 

