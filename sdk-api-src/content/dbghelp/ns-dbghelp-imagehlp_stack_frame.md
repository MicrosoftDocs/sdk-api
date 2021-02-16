---
UID: NS:dbghelp._IMAGEHLP_STACK_FRAME
title: IMAGEHLP_STACK_FRAME (dbghelp.h)
description: Contains the stack frame information.
helpviewer_keywords: ["*PIMAGEHLP_STACK_FRAME","IMAGEHLP_STACK_FRAME","IMAGEHLP_STACK_FRAME structure","PIMAGEHLP_STACK_FRAME","PIMAGEHLP_STACK_FRAME structure pointer","_IMAGEHLP_STACK_FRAME","_win32_imagehlp_stack_frame_str","base.imagehlp_stack_frame_str","dbghelp/IMAGEHLP_STACK_FRAME","dbghelp/PIMAGEHLP_STACK_FRAME"]
old-location: base\imagehlp_stack_frame_str.htm
tech.root: Debug
ms.assetid: b6c89cf2-b108-4518-9f4c-4a3684b3f0a7
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_STACK_FRAME, IMAGEHLP_STACK_FRAME, IMAGEHLP_STACK_FRAME structure, PIMAGEHLP_STACK_FRAME, PIMAGEHLP_STACK_FRAME structure pointer, _IMAGEHLP_STACK_FRAME, _win32_imagehlp_stack_frame_str, base.imagehlp_stack_frame_str, dbghelp/IMAGEHLP_STACK_FRAME, dbghelp/PIMAGEHLP_STACK_FRAME'
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
req.typenames: IMAGEHLP_STACK_FRAME, *PIMAGEHLP_STACK_FRAME
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_STACK_FRAME
 - dbghelp/_IMAGEHLP_STACK_FRAME
 - PIMAGEHLP_STACK_FRAME
 - dbghelp/PIMAGEHLP_STACK_FRAME
 - IMAGEHLP_STACK_FRAME
 - dbghelp/IMAGEHLP_STACK_FRAME
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
 - IMAGEHLP_STACK_FRAME
---

# IMAGEHLP_STACK_FRAME structure


## -description

Contains the stack frame information. This structure is used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.

## -struct-fields

### -field InstructionOffset

The program counter. 




<b>x86:  </b>The program counter is EIP.

<b>Intel Itanium:  </b>The program counter is a combination of the bundle address and a slot indicator of 0, 4, or 8 for the slot within the bundle.

<b>x64:  </b>The program counter is RIP.

### -field ReturnOffset

The return address.

### -field FrameOffset

The frame pointer. 




<b>x86:  </b>The frame pointer is EBP.

<b>Intel Itanium:  </b>There is no frame pointer, but <b>AddrBStore</b> is used.

<b>x64:  </b>The frame pointer is RBP. AMD-64 does not always use this value.

### -field StackOffset

The stack pointer. 




<b>x86:  </b>The stack pointer is ESP.

<b>Intel Itanium:  </b>The stack pointer is SP.

<b>x64:  </b>The stack pointer is RSP.

### -field BackingStoreOffset

<b>Intel Itanium:  </b>The backing store address.

### -field FuncTableEntry

<b>x86:  </b>An 
<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a> structure. If there is no function table entry, this member is <b>NULL</b>.

### -field Params

The possible arguments to the function.

### -field Reserved

This member is reserved for system use.

### -field Virtual

If this is a virtual frame, this member is <b>TRUE</b>. Otherwise, this member is <b>FALSE</b>.

### -field Reserved2

This member is reserved for system use.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a>