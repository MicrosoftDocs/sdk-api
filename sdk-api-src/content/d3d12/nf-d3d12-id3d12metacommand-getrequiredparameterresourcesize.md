---
UID: NF:d3d12.ID3D12MetaCommand.GetRequiredParameterResourceSize
title: ID3D12MetaCommand::GetRequiredParameterResourceSize
author: windows-sdk-content
description: Retrieves the amount of memory required for the specified runtime parameter resource for a meta command, for the specified stage.
old-location: direct3d12\id3d12metacommand_getrequiredparameterresourcesize.htm
tech.root: direct3d12
ms.assetid: DE619146-CEF7-4D8C-A4E7-D2BCE1BD1FBC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRequiredParameterResourceSize, GetRequiredParameterResourceSize method, GetRequiredParameterResourceSize method,ID3D12MetaCommand interface, ID3D12MetaCommand interface,GetRequiredParameterResourceSize method, ID3D12MetaCommand.GetRequiredParameterResourceSize, ID3D12MetaCommand::GetRequiredParameterResourceSize, d3d12/ID3D12MetaCommand::GetRequiredParameterResourceSize, direct3d12.id3d12metacommand_getrequiredparameterresourcesize
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
 - ID3D12MetaCommand.GetRequiredParameterResourceSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12MetaCommand::GetRequiredParameterResourceSize


## -description


Retrieves the amount of memory required for the  specified  runtime parameter resource for a meta command, for the specified stage.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/1A3278EE-5D46-4E18-9F10-47001506C3DC">D3D12_META_COMMAND_PARAMETER_STAGE</a></b>

A <a href="https://msdn.microsoft.com/1A3278EE-5D46-4E18-9F10-47001506C3DC">D3D12_META_COMMAND_PARAMETER_STAGE</a> specifying the stage to which the parameter belongs.


### -param ParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index of the parameter within the stage.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The number of bytes required for the  specified  runtime parameter resource.




## -see-also




<a href="https://msdn.microsoft.com/976A7F78-1801-47DD-9350-21F530B4D145">ID3D12MetaCommand</a>
 

 

