---
UID: NF:atlthunk.AtlThunk_InitData
title: AtlThunk_InitData function
author: windows-sdk-content
description: Initializes an ATL thunk.
old-location: base\atlthunk_initdata.htm
tech.root: memory
ms.assetid: 550EF700-56DC-4516-A724-0F7ADECC17C9
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AtlThunk_InitData, AtlThunk_InitData function, atlthunk/AtlThunk_InitData, base.atlthunk_initdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: atlthunk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Atlthunk.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - atlthunk.dll
api_name:
 - AtlThunk_InitData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



