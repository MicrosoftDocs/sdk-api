---
UID: NF:shlwapi.SHGlobalCounterDecrement
title: SHGlobalCounterDecrement function (shlwapi.h)
description: Decrements a global counter.
helpviewer_keywords: ["SHGlobalCounterDecrement","SHGlobalCounterDecrement function [Windows Shell]","_shell_SHGlobalCounterDecrement","shell.SHGlobalCounterDecrement","shlwapi/SHGlobalCounterDecrement"]
old-location: shell\SHGlobalCounterDecrement.htm
tech.root: shell
ms.assetid: 67b45cb9-9d8d-48ef-a7bc-9cd8824bdf2b
ms.date: 12/05/2018
ms.keywords: SHGlobalCounterDecrement, SHGlobalCounterDecrement function [Windows Shell], _shell_SHGlobalCounterDecrement, shell.SHGlobalCounterDecrement, shlwapi/SHGlobalCounterDecrement
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
 - SHGlobalCounterDecrement
 - shlwapi/SHGlobalCounterDecrement
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
 - SHGlobalCounterDecrement
---

# SHGlobalCounterDecrement function


## -description

Decrements a global counter.

## -parameters

### -param id [in]

Type: <b>const <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a> to decrement.

## -returns

Type: <b>long</b>

The value of the counter after the decrement.

## -see-also

<a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcountergetvalue">SHGlobalCounterGetValue</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcounterincrement">SHGlobalCounterIncrement</a>