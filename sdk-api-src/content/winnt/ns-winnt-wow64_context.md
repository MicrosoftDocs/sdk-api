---
UID: NS:winnt._WOW64_CONTEXT
title: WOW64_CONTEXT (winnt.h)
description: Represents a context frame on WOW64.
helpviewer_keywords: ["*PWOW64_CONTEXT","PWOW64_CONTEXT","PWOW64_CONTEXT structure pointer","WOW64_CONTEXT","WOW64_CONTEXT structure","_WOW64_CONTEXT","base.wow64_context","winnt/PWOW64_CONTEXT","winnt/WOW64_CONTEXT"]
old-location: base\wow64_context.htm
tech.root: Debug
ms.assetid: b27205a2-2c33-4f45-8948-9919bcd2355a
ms.date: 12/05/2018
ms.keywords: '*PWOW64_CONTEXT, PWOW64_CONTEXT, PWOW64_CONTEXT structure pointer, WOW64_CONTEXT, WOW64_CONTEXT structure, _WOW64_CONTEXT, base.wow64_context, winnt/PWOW64_CONTEXT, winnt/WOW64_CONTEXT'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WOW64_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WOW64_CONTEXT
 - winnt/_WOW64_CONTEXT
 - WOW64_CONTEXT
 - winnt/WOW64_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - WOW64_CONTEXT
---

# WOW64_CONTEXT structure


## -description

Represents a context frame on WOW64. Refer to the header file WinNT.h for the definition of this structure.

## -struct-fields

## -remarks

In the following versions of Windows, Slot 1 of Thread Local Storage (TLS) holds a pointer to a structure that contains a <b>WOW64_CONTEXT</b> structure starting at offset 4. This might change in later versions of Windows.

<table>
<tr>
<td>Windows Vista</td>
<td>Windows Server 2008</td>
</tr>
<tr>
<td>Windows 7</td>
<td>Windows Server 2008 R2</td>
</tr>
<tr>
<td>Windows 8</td>
<td>Windows Server 2012</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>Windows Server 2012 R2</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Debug/thread-environment-block--debugging-notes-">Thread Environment Block (Debugging Notes)</a>



<a href="/windows/desktop/api/winnt/ns-winnt-wow64_floating_save_area">WOW64_FLOATING_SAVE_AREA</a>



<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64getthreadcontext.md">Wow64GetThreadContext</a>



<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64setthreadcontext.md">Wow64SetThreadContext</a>