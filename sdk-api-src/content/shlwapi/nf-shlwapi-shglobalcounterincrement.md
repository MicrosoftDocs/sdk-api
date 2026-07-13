---
UID: NF:shlwapi.SHGlobalCounterIncrement
title: SHGlobalCounterIncrement function (shlwapi.h)
description: Increments a global counter.
helpviewer_keywords: ["SHGlobalCounterIncrement","SHGlobalCounterIncrement function [Windows Shell]","_shell_SHGlobalCounterIncrement","shell.SHGlobalCounterIncrement","shlwapi/SHGlobalCounterIncrement"]
old-location: shell\SHGlobalCounterIncrement.htm
tech.root: shell
ms.assetid: 088efa01-b070-4384-b17a-311aefb0737c
ms.date: 12/05/2018
ms.keywords: SHGlobalCounterIncrement, SHGlobalCounterIncrement function [Windows Shell], _shell_SHGlobalCounterIncrement, shell.SHGlobalCounterIncrement, shlwapi/SHGlobalCounterIncrement
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
 - SHGlobalCounterIncrement
 - shlwapi/SHGlobalCounterIncrement
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
 - SHGlobalCounterIncrement
---

# SHGlobalCounterIncrement function


## -description

Increments a global counter.

## -parameters

### -param id [in]

Type: <b>const <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a> to increment.

## -returns

Type: <b>long</b>

The value of the counter after the increment.

## -see-also

<a href="/windows/desktop/api/shlwapi/ne-shlwapi-shglobalcounter">SHGLOBALCOUNTER</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcounterdecrement">SHGlobalCounterDecrement</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shglobalcountergetvalue">SHGlobalCounterGetValue</a>