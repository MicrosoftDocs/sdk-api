---
UID: NF:d3d12.ID3D12GraphicsCommandList4.InitializeMetaCommand
title: ID3D12GraphicsCommandList4::InitializeMetaCommand (d3d12.h)
author: windows-sdk-content
description: Initializes the specified meta command.
old-location: direct3d12\id3d12graphicscommandlist4_initializemetacommand.htm
tech.root: direct3d12
ms.assetid: EC50FE25-27C7-4A5D-B4D1-57D402730AF0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList4 interface,InitializeMetaCommand method, ID3D12GraphicsCommandList4.InitializeMetaCommand, ID3D12GraphicsCommandList4::InitializeMetaCommand, InitializeMetaCommand, InitializeMetaCommand method, InitializeMetaCommand method,ID3D12GraphicsCommandList4 interface, d3d12/ID3D12GraphicsCommandList4::InitializeMetaCommand, direct3d12.id3d12graphicscommandlist4_initializemetacommand
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.h
api_name:
 - ID3D12GraphicsCommandList4.InitializeMetaCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12GraphicsCommandList4::InitializeMetaCommand


## -description


Initializes the specified meta command.

You must initialize a meta command at least once prior (on the GPU's timeline) to executing it. Initializing gives the  implementation the chance to perform any work necessary to accelerate the invocation of the meta command. You must supply the sufficient resource parameters, including the persistent cache resource.


## -parameters




### -param pMetaCommand [in]

A pointer to an <a href="https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/nn-d3d12-id3d12metacommand">ID3D12MetaCommand</a> representing the meta command to initialize.


### -param pInitializationParametersData [in, optional]

An optional pointer to a constant structure containing the values of the parameters for initializing the meta command.


### -param InitializationParametersDataSizeInBytes [in]

A <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a> containing the size of the structure pointed to by <i>pInitializationParametersData</i>, if set, otherwise 0.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt847460(v=VS.85).aspx">ID3D12GraphicsCommandList4</a>
 

 

