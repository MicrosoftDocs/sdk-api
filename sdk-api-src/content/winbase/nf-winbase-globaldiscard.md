---
UID: NF:winbase.GlobalDiscard
title: GlobalDiscard macro (winbase.h)
description: Discards the specified global memory block.
helpviewer_keywords: ["GlobalDiscard","GlobalDiscard macro","_win32_globaldiscard","base.globaldiscard","winbase/GlobalDiscard"]
old-location: base\globaldiscard.htm
tech.root: base
ms.assetid: af6160ce-ab7a-4198-bca3-dd5d51cacfa5
ms.date: 12/05/2018
ms.keywords: GlobalDiscard, GlobalDiscard macro, _win32_globaldiscard, base.globaldiscard, winbase/GlobalDiscard
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GlobalDiscard
 - winbase/GlobalDiscard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - GlobalDiscard
---

# GlobalDiscard macro


## -description

Discards the specified global memory block. The lock count of the memory object must be zero.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param h [in]

A handle to the global memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function.

## -remarks

Although 
<b>GlobalDiscard</b> discards the object's memory block, the handle to the object remains valid. The process can subsequently pass the handle to the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function to allocate another global memory block identified by the same handle.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>