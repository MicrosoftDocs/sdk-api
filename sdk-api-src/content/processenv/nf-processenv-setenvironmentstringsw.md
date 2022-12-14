---
UID: NF:processenv.SetEnvironmentStringsW
title: SetEnvironmentStringsW
description: The SetEnvironmentStringsW (Unicode) function (processenv.h) sets the environment strings of the calling process for the current process.
ms.date: 08/05/2022
ms.keywords: SetEnvironmentStringsW
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: processenv.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - SetEnvironmentStringsW
 - processenv/SetEnvironmentStringsW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - api-ms-win-core-processenvironment-l1-1-0.dll
 - kernelbase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - SetEnvironmentStringsW
---

## -description

Sets the environment strings of the calling process (both the system and the user environment variables) for the current process.

## -parameters

### -param NewEnvironment

The environment variable string using the following format:

<i>Var1</i>
<i>Value1</i>
<i>Var2</i>
<i>Value2</i>
<i>Var3</i>
<i>Value3</i>
<i>VarN</i>
<i>ValueN</i>

## -returns

Returns S_OK on success.

## -remarks

## -see-also

