---
UID: NF:shlwapi.SHIsLowMemoryMachine
title: SHIsLowMemoryMachine function (shlwapi.h)
description: Not supported. (SHIsLowMemoryMachine)
helpviewer_keywords: ["ILMM_IE4","SHIsLowMemoryMachine","SHIsLowMemoryMachine function [Windows Shell]","_shell_SHIsLowMemoryMachine","shell.SHIsLowMemoryMachine","shlwapi/SHIsLowMemoryMachine"]
old-location: shell\SHIsLowMemoryMachine.htm
tech.root: shell
ms.assetid: 3a91156d-eef9-4d3c-9cb8-fd50bfa94354
ms.date: 12/05/2018
ms.keywords: ILMM_IE4, SHIsLowMemoryMachine, SHIsLowMemoryMachine function [Windows Shell], _shell_SHIsLowMemoryMachine, shell.SHIsLowMemoryMachine, shlwapi/SHIsLowMemoryMachine
req.header: shlwapi.h
req.include-header: Shlwapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHIsLowMemoryMachine
 - shlwapi/SHIsLowMemoryMachine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHIsLowMemoryMachine
---

# SHIsLowMemoryMachine function


## -description

Not supported.

## -parameters

### -param dwType [in]

Type: <b>DWORD</b>

The type of machine being examined. The following is the only recognized value.



#### ILMM_IE4

An older (circa 1997), low-end machine. Since system resources in general were lower on these older machines, the low-memory threshold is accordingly lower.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the machine is considered low on resources, <b>FALSE</b> otherwise.

<div class="alert"><b>Note</b>  Always returns <b>FALSE</b> under Windows XP.</div>
<div> </div>

