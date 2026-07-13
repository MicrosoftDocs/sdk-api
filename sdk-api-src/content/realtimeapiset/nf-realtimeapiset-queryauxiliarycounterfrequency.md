---
UID: NF:realtimeapiset.QueryAuxiliaryCounterFrequency
title: QueryAuxiliaryCounterFrequency function (realtimeapiset.h)
description: Queries the auxiliary counter frequency.
helpviewer_keywords: ["QueryAuxiliaryCounterFrequency","QueryAuxiliaryCounterFrequency function","base.queryauxiliarycounterfrequency","realtimeapiset/QueryAuxiliaryCounterFrequency"]
old-location: base\queryauxiliarycounterfrequency.htm
tech.root: winprog
ms.assetid: 71E00DF2-7F67-43D2-9D6D-BFE9FEA4B30A
ms.date: 12/05/2018
ms.keywords: QueryAuxiliaryCounterFrequency, QueryAuxiliaryCounterFrequency function, base.queryauxiliarycounterfrequency, realtimeapiset/QueryAuxiliaryCounterFrequency
req.header: realtimeapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryAuxiliaryCounterFrequency
 - realtimeapiset/QueryAuxiliaryCounterFrequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-realtime-l1-1-2.dll
 - Kernel32.dll
api_name:
 - QueryAuxiliaryCounterFrequency
---

# QueryAuxiliaryCounterFrequency function


## -description

Queries the auxiliary counter frequency.

## -parameters

### -param lpAuxiliaryCounterFrequency [out]

Long pointer to an output buffer that contains the specified auxiliary counter frequency. If the auxiliary counter is not supported, the value in the output buffer will be undefined.

## -returns

Returns <b>S_OK</b> if the auxiliary counter is supported and <b>E_NOTIMPL</b> if the auxiliary counter is not supported.

## -remarks

You can determine the availability of the auxiliary counter by comparing the returned value against <b>E_NOTIMPL</b>.


#### Examples

The following sample describes how to call <b>QueryAuxiliaryCounterFrequency</b> to retrieve the counter frequency.


```cpp
#include <stdio.h> 
#include <windows.h> 
int 
wmain (int argc, wchar_t* argv[]) 
{

   ULONGLONG AuxiliaryCounterFrequency;
   HRESULT Result;

   Result = QueryAuxiliaryCounterFrequency(&AuxiliaryCounterFrequency); 
   if (SUCCEEDED(Result)) {
      wprintf(L"Auxiliary counter frequency is: %llu.\n", AuxiliaryCounterFrequency);
   } 
   else if (Result == E_NOTIMPL) {
      wprintf(L"Auxiliary counter is not supported.\n"); 
   }
	  else {
    wprintf(L"Error code: 0x%x.\n", Result);
   }

   return 0; 
} 

```

