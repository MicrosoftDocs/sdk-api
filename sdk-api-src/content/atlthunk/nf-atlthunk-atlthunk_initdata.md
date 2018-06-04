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

# AtlThunk_InitData function


## -description


Initializes an ATL thunk.


## -parameters




### -param Thunk

A non-null return value from <a href="https://msdn.microsoft.com/D306E6CB-72D4-4820-885E-175FC8500954">AtlThunk_AllocateData</a>.


### -param Proc

See the example in remarks for more info.


### -param FirstParameter

See the example in remarks for more info.


## -returns



This function does not return a value.




## -remarks



An ATL thunk has a signature of WNDPROC. See the following sample for more info on an implementation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> LRESULT CALLBACK AtlThunk(  
   _In_ HWND   hwnd,  
   _In_ UINT   uMsg,  
   _In_ WPARAM wParam, 
   _In_ LPARAM lParam  
   )  
 {  
   static void* FirstParameter; 
   static WNDPROC Proc; 
   return Proc((HWND)FirstParameter, uMsg, wParam, lParam); 
 } 
</pre>
</td>
</tr>
</table></span></div>
An arbitrary number of AtlThunk functions can be created; FirstParameter and Proc are set (differently) for each one.



