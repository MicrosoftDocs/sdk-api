---
UID: NF:winbase.GlobalDiscard
title: GlobalDiscard macro
author: windows-sdk-content
description: Discards the specified global memory block.
old-location: base\globaldiscard.htm
tech.root: memory
ms.assetid: af6160ce-ab7a-4198-bca3-dd5d51cacfa5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GlobalDiscard, GlobalDiscard macro, _win32_globaldiscard, base.globaldiscard, winbase/GlobalDiscard
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - GlobalDiscard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalDiscard macro


## -description


Discards the specified global memory block. The lock count of the memory object must be zero.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.
</div><div> </div>

## -parameters




### -param h [in]

A handle to the global memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.


## -remarks



Although 
<b>GlobalDiscard</b> discards the object's memory block, the handle to the object remains valid. The process can subsequently pass the handle to the 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function to allocate another global memory block identified by the same handle.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

