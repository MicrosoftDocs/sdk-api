---
UID: NF:atlthunk.AtlThunk_InitData
title: AtlThunk_InitData function (atlthunk.h)
description: Initializes an ATL thunk.
helpviewer_keywords: ["AtlThunk_InitData","AtlThunk_InitData function","atlthunk/AtlThunk_InitData","base.atlthunk_initdata"]
old-location: base\atlthunk_initdata.htm
tech.root: base
ms.assetid: 550EF700-56DC-4516-A724-0F7ADECC17C9
ms.date: 12/05/2018
ms.keywords: AtlThunk_InitData, AtlThunk_InitData function, atlthunk/AtlThunk_InitData, base.atlthunk_initdata
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AtlThunk_InitData
 - atlthunk/AtlThunk_InitData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - atlthunk.dll
api_name:
 - AtlThunk_InitData
---

# AtlThunk_InitData function


## -description

Initializes an ATL thunk.

## -parameters

### -param Thunk

A non-null return value from <a href="/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata">AtlThunk_AllocateData</a>.

### -param Proc

See the example in remarks for more info.

### -param FirstParameter

See the example in remarks for more info.

## -remarks

An ATL thunk has a signature of WNDPROC. See the following sample for more info on an implementation.


```cpp
 LRESULT CALLBACK AtlThunk(  
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

```


An arbitrary number of AtlThunk functions can be created; FirstParameter and Proc are set (differently) for each one.