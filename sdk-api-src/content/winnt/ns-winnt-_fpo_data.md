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

# _FPO_DATA structure


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




<a href="https://msdn.microsoft.com/387c20b0-ed16-463c-8b11-3ac9a43548a1">FunctionTableAccessProc64</a>



<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a>



<a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a>
 

 

