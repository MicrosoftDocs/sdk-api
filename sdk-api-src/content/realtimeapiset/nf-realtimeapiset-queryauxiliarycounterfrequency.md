---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


