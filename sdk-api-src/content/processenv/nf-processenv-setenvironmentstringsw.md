---
UID: NF:processenv.SetEnvironmentStringsW
title: SetEnvironmentStringsW
ms.date: 4/26/2019
ms.keywords: SetEnvironmentStringsW
f1_keywords:
- SetEnvironmentStringsW
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: processenv.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- DllExport
api_location:
- api-ms-win-core-processenvironment-l1-1-0.dll
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

