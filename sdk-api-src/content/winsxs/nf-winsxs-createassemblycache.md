---
UID: NF:winsxs.CreateAssemblyCache
title: CreateAssemblyCache function (winsxs.h)
description: The CreateAssemblyCache function obtains an instance of the IAssemblyCache interface.
helpviewer_keywords: ["CreateAssemblyCache","CreateAssemblyCache function [Side-by-side Assemblies]","setup.createassemblycache","winsxs/CreateAssemblyCache"]
old-location: setup\createassemblycache.htm
tech.root: SbsCs
ms.assetid: 99032c27-d9a3-4319-ba6e-2271d35da804
ms.date: 12/05/2018
ms.keywords: CreateAssemblyCache, CreateAssemblyCache function [Side-by-side Assemblies], setup.createassemblycache, winsxs/CreateAssemblyCache
f1_keywords:
- winsxs/CreateAssemblyCache
dev_langs:
- c++
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Sxs.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- sxs.dll
api_name:
- CreateAssemblyCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateAssemblyCache function


## -description


The <b>CreateAssemblyCache</b> function obtains an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nn-winsxs-iassemblycache">IAssemblyCache</a> interface.


## -parameters




### -param ppAsmCache

Pointer the location that receives the <a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nn-winsxs-iassemblycache">IAssemblyCache</a> pointer.


### -param dwReserved

Reserved.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



