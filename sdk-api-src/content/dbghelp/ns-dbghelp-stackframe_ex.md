---
UID: NS:dbghelp._tagSTACKFRAME_EX
title: STACKFRAME_EX (dbghelp.h)
description: Represents an extended stack frame.
helpviewer_keywords: ["*LPSTACKFRAME_EX","INLINE_FRAME_CONTEXT_IGNORE","INLINE_FRAME_CONTEXT_INIT","LPSTACKFRAME_EX","LPSTACKFRAME_EX structure pointer","STACKFRAME_EX","STACKFRAME_EX structure","_tagSTACKFRAME_EX","base.stackframe_ex","dbghelp/LPSTACKFRAME_EX","dbghelp/STACKFRAME_EX"]
old-location: base\stackframe_ex.htm
tech.root: Debug
ms.assetid: d4606619-f9c5-41e9-8627-17846b98956a
ms.date: 12/05/2018
ms.keywords: '*LPSTACKFRAME_EX, INLINE_FRAME_CONTEXT_IGNORE, INLINE_FRAME_CONTEXT_INIT, LPSTACKFRAME_EX, LPSTACKFRAME_EX structure pointer, STACKFRAME_EX, STACKFRAME_EX structure, _tagSTACKFRAME_EX, base.stackframe_ex, dbghelp/LPSTACKFRAME_EX, dbghelp/STACKFRAME_EX'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STACKFRAME_EX, *LPSTACKFRAME_EX
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - _tagSTACKFRAME_EX
 - dbghelp/_tagSTACKFRAME_EX
 - LPSTACKFRAME_EX
 - dbghelp/LPSTACKFRAME_EX
 - STACKFRAME_EX
 - dbghelp/STACKFRAME_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - STACKFRAME_EX
---

# STACKFRAME_EX structure


## -description

Represents an extended stack frame.

## -struct-fields

### -field AddrPC

An <a href="/windows/desktop/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the program 
      counter.
      

<b>x86:  </b>The program counter is EIP.

<b>Intel Itanium:  </b>The program counter is StIIP.

<b>x64:  </b>The program counter is RIP.

### -field AddrReturn

An <a href="/windows/desktop/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies 
      the return address.

### -field AddrFrame

An <a href="/windows/desktop/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies 
      the frame pointer.
      

<b>x86:  </b>The frame pointer is EBP.

<b>Intel Itanium:  </b>There is no frame pointer, but <b>AddrBStore</b> is used.

<b>x64:  </b>The frame pointer is RBP or RDI. This value is not always used.

### -field AddrStack

An <a href="/windows/desktop/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies 
      the stack pointer.
      

<b>x86:  </b>The stack pointer is ESP.

<b>Intel Itanium:  </b>The stack pointer is SP.

<b>x64:  </b>The stack pointer is RSP.

### -field AddrBStore

<b>Intel Itanium:  </b>An <a href="/windows/desktop/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies 
        the backing store (RsBSP).

### -field FuncTableEntry

On x86 computers, this member is an <a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a> 
      structure. If there is no function table entry, this member is <b>NULL</b>.

### -field Params

The possible arguments to the function.

### -field Far

This member is <b>TRUE</b> if this is a WOW far call.

### -field Virtual

This member is <b>TRUE</b> if this is a virtual frame.

### -field Reserved

This member is used internally by the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk64">StackWalk64</a> 
      function.

### -field KdHelp

A <a href="/windows/desktop/api/dbghelp/ns-dbghelp-kdhelp64">KDHELP64</a> structure that specifies helper data for 
      walking kernel callback frames.

### -field StackFrameSize

Set to <code>sizeof(STACKFRAME_EX)</code>.

### -field InlineFrameContext

Specifies the type of the inline frame context.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%"><a id="inline_frame_context_init"></a><a id="INLINE_FRAME_CONTEXT_INIT"></a><dl>
<dt><b>INLINE_FRAME_CONTEXT_INIT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unknown.
</td>
</tr>

<tr>
<td width="40%"><a id="inline_frame_context_ignore"></a><a id="INLINE_FRAME_CONTEXT_IGNORE"></a><dl>
<dt><b>INLINE_FRAME_CONTEXT_IGNORE</b></dt>
<dt>0xffffffff</dt>
</dl>
</td>
<td width="60%">
Unknown.
</td>
</tr>

</table>

## -remarks

This structure supersedes the <b>STACKFRAME64</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>.
