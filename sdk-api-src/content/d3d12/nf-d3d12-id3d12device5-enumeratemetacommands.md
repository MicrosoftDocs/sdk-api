---
UID: NF:d3d12.ID3D12Device5.EnumerateMetaCommands
title: ID3D12Device5::EnumerateMetaCommands (d3d12.h)
description: Queries reflection metadata about available meta commands.
old-location: direct3d12\id3d12device5_enumeratemetacommands.htm
tech.root: direct3d12
ms.assetid: 71A16704-487F-49AA-B229-61CCD15B3037
ms.date: 12/05/2018
ms.keywords: EnumerateMetaCommands, EnumerateMetaCommands method, EnumerateMetaCommands method,ID3D12Device5 interface, ID3D12Device5 interface,EnumerateMetaCommands method, ID3D12Device5.EnumerateMetaCommands, ID3D12Device5::EnumerateMetaCommands, d3d12/ID3D12Device5::EnumerateMetaCommands, direct3d12.id3d12device5_enumeratemetacommands
f1_keywords:
- d3d12/ID3D12Device5.EnumerateMetaCommands
dev_langs:
- c++
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
- ID3D12Device5.EnumerateMetaCommands
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device5::EnumerateMetaCommands


## -description


Queries reflection metadata about available meta commands.


## -parameters




### -param pNumMetaCommands [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a> containing the number of meta commands to query for. This field determines the size of the <i>pDescs</i> array, unless <i>pDescs</i> is <b>nullptr</b>.


### -param pDescs [out, optional]

Type: <b>D3D12_META_COMMAND_DESC*</b>

An optional pointer to an array of  <a href="https://msdn.microsoft.com/0783068A-21D0-4316-9F50-8566535747C8">D3D12_META_COMMAND_DESC</a> containing the descriptions of the available meta commands. Pass <b>nullptr</b> to have the number of available meta commands returned in <i>pNumMetaCommands</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt847457(v=VS.85).aspx">ID3D12Device5</a>
 

 

