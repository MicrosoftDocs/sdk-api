---
UID: NF:shlwapi.SHGlobalCounterGetValue
title: SHGlobalCounterGetValue function (shlwapi.h)
description: Gets the current value of a global counter.
helpviewer_keywords: ["SHGlobalCounterGetValue","SHGlobalCounterGetValue function [Windows Shell]","_shell_SHGlobalCounterGetValue","shell.SHGlobalCounterGetValue","shlwapi/SHGlobalCounterGetValue"]
old-location: shell\SHGlobalCounterGetValue.htm
tech.root: shell
ms.assetid: cf158770-c9af-4488-9ed0-486e9a528a65
ms.date: 12/05/2018
ms.keywords: SHGlobalCounterGetValue, SHGlobalCounterGetValue function [Windows Shell], _shell_SHGlobalCounterGetValue, shell.SHGlobalCounterGetValue, shlwapi/SHGlobalCounterGetValue
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ShLwApi.Lib
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGlobalCounterGetValue
 - shlwapi/SHGlobalCounterGetValue
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
 - SHGlobalCounterGetValue
---

# SHGlobalCounterGetValue function


## -description

Gets the current value of a global counter.

## -parameters

### -param id [in]

Type: <b>const <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a> for which to retrieve the current value.

## -returns

Type: <b>long</b>

The current value of the counter.

## -see-also

<a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcounterdecrement">SHGlobalCounterDecrement</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcounterincrement">SHGlobalCounterIncrement</a>