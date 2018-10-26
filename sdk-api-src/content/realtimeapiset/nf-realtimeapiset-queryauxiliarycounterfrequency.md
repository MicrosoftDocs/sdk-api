---
UID: NF:realtimeapiset.QueryAuxiliaryCounterFrequency
title: QueryAuxiliaryCounterFrequency function
author: windows-sdk-content
description: Queries the auxiliary counter frequency.
old-location: base\queryauxiliarycounterfrequency.htm
tech.root: sysinfo
ms.assetid: 71E00DF2-7F67-43D2-9D6D-BFE9FEA4B30A
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: QueryAuxiliaryCounterFrequency, QueryAuxiliaryCounterFrequency function, base.queryauxiliarycounterfrequency, realtimeapiset/QueryAuxiliaryCounterFrequency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - QueryAuxiliaryCounterFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;stdio.h&gt; 
#include &lt;windows.h&gt; 
int 
wmain (int argc, wchar_t* argv[]) 
{

   ULONGLONG AuxiliaryCounterFrequency;
   HRESULT Result;

   Result = QueryAuxiliaryCounterFrequency(&amp;AuxiliaryCounterFrequency); 
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
</pre>
</td>
</tr>
</table></span></div>


