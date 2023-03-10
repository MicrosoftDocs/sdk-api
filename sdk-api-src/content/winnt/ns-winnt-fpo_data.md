---
UID: NS:winnt._FPO_DATA
title: FPO_DATA (winnt.h)
description: Represents the stack frame layout for a function on an x86 computer when frame pointer omission (FPO) optimization is used. The structure is used to locate the base of the call frame.
helpviewer_keywords: ["*PFPO_DATA","FPO_DATA","FPO_DATA structure","FRAME_FPO","FRAME_NONFPO","FRAME_TRAP","FRAME_TSS","PFPO_DATA","PFPO_DATA structure pointer","_FPO_DATA","_win32_fpo_data_str","base.fpo_data_str","winnt/FPO_DATA","winnt/PFPO_DATA"]
old-location: base\fpo_data_str.htm
tech.root: Debug
ms.assetid: 916dc7d5-ed88-4573-b696-fd00bbf4e086
ms.date: 12/05/2018
ms.keywords: '*PFPO_DATA, FPO_DATA, FPO_DATA structure, FRAME_FPO, FRAME_NONFPO, FRAME_TRAP, FRAME_TSS, PFPO_DATA, PFPO_DATA structure pointer, _FPO_DATA, _win32_fpo_data_str, base.fpo_data_str, winnt/FPO_DATA, winnt/PFPO_DATA'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: FPO_DATA, *PFPO_DATA
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _FPO_DATA
 - winnt/_FPO_DATA
 - PFPO_DATA
 - winnt/PFPO_DATA
 - FPO_DATA
 - winnt/FPO_DATA
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
 - FPO_DATA
---

# FPO_DATA structure


## -description

Represents the stack frame layout for a function on an x86 computer when frame pointer omission (FPO) optimization is used. The structure is used to locate the base of the call frame.

## -struct-fields

### -field ulOffStart

The offset of the first byte of the function code.

### -field cbProcSize

The number of bytes in the function.

### -field cdwLocals

The number of local variables.

### -field cdwParams

The size of the parameters, in <b>DWORD</b>s.

### -field cbProlog

The number of bytes in the function prolog code.

### -field cbRegs

The number of registers saved.

### -field fHasSEH

A variable that indicates whether the function uses structured exception handling.

### -field fUseBP

A variable that indicates whether the EBP register has been allocated.

### -field reserved

Reserved for future use.

### -field cbFrame

A variable that indicates the frame type.

<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FRAME_FPO"></a><a id="frame_fpo"></a><dl>
<dt><b>FRAME_FPO</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
FPO frame

</td>
</tr>
<tr>
<td width="40%"><a id="FRAME_NONFPO"></a><a id="frame_nonfpo"></a><dl>
<dt><b>FRAME_NONFPO</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Non-FPO frame

</td>
</tr>
<tr>
<td width="40%"><a id="FRAME_TRAP"></a><a id="frame_trap"></a><dl>
<dt><b>FRAME_TRAP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Trap frame

</td>
</tr>
<tr>
<td width="40%"><a id="FRAME_TSS"></a><a id="frame_tss"></a><dl>
<dt><b>FRAME_TSS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
TSS frame

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfunction_table_access_routine">FunctionTableAccessProc64</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-stackframe">STACKFRAME64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a>