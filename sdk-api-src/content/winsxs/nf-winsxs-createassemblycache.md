---
UID: NF:winsxs.CreateAssemblyCache
title: CreateAssemblyCache function
author: windows-sdk-content
description: The CreateAssemblyCache function obtains an instance of the IAssemblyCache interface.
old-location: setup\createassemblycache.htm
tech.root: SbsCs
ms.assetid: 99032c27-d9a3-4319-ba6e-2271d35da804
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateAssemblyCache, CreateAssemblyCache function [Side-by-side Assemblies], setup.createassemblycache, winsxs/CreateAssemblyCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateAssemblyCache function


## -description


The <b>CreateAssemblyCache</b> function obtains an instance of the <a href="https://msdn.microsoft.com/6c411ae7-5a8f-47ca-a9c1-e23000f64620">IAssemblyCache</a> interface.


## -parameters




### -param ppAsmCache

Pointer the location that receives the <a href="https://msdn.microsoft.com/6c411ae7-5a8f-47ca-a9c1-e23000f64620">IAssemblyCache</a> pointer.


### -param dwReserved

Reserved.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



