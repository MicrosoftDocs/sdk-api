---
UID: NS:dbghelp._tagSTACKFRAME_EX
title: "_tagSTACKFRAME_EX"
author: windows-sdk-content
description: Represents an extended stack frame.
old-location: base\stackframe_ex.htm
tech.root: Debug
ms.assetid: d4606619-f9c5-41e9-8627-17846b98956a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPSTACKFRAME_EX, INLINE_FRAME_CONTEXT_IGNORE, INLINE_FRAME_CONTEXT_INIT, LPSTACKFRAME_EX, LPSTACKFRAME_EX structure pointer, STACKFRAME_EX, STACKFRAME_EX structure, _tagSTACKFRAME_EX, base.stackframe_ex, dbghelp/LPSTACKFRAME_EX, dbghelp/STACKFRAME_EX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - STACKFRAME_EX
product: Windows
targetos: Windows
req.typenames: STACKFRAME_EX, *LPSTACKFRAME_EX
req.redist: DbgHelp.dll 6.2 or later
---

# _tagSTACKFRAME_EX structure


## -description


Represents an extended stack frame.


## -struct-fields




### -field AddrPC

An <a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the program 
      counter.
      

<b>x86:  </b>The program counter is EIP.

<b>Intel Itanium:  </b>The program counter is StIIP.

<b>x64:  </b>The program counter is RIP.


### -field AddrReturn

An <a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies 
      the return address.


### -field AddrFrame

An <a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies 
      the frame pointer.
      

<b>x86:  </b>The frame pointer is EBP.

<b>Intel Itanium:  </b>There is no frame pointer, but <b>AddrBStore</b> is used.

<b>x64:  </b>The frame pointer is RBP or RDI. This value is not always used.


### -field AddrStack

An <a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies 
      the stack pointer.
      

<b>x86:  </b>The stack pointer is ESP.

<b>Intel Itanium:  </b>The stack pointer is SP.

<b>x64:  </b>The stack pointer is RSP.


### -field AddrBStore

<b>Intel Itanium:  </b>An <a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies 
        the backing store (RsBSP).


### -field FuncTableEntry

On x86 computers, this member is an <a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a> 
      structure. If there is no function table entry, this member is <b>NULL</b>.


### -field Params

The possible arguments to the function.


### -field Far

This member is <b>TRUE</b> if this is a WOW far call.


### -field Virtual

This member is <b>TRUE</b> if this is a virtual frame.


### -field Reserved

This member is used internally by the <a href="https://msdn.microsoft.com/87765e30-b444-4f68-b11f-1be73e0775fc">StackWalkEx</a> 
      function.


### -field KdHelp

A <a href="https://msdn.microsoft.com/da31c92c-0257-4ae2-8d69-ea8cd58adc10">KDHELP64</a> structure that specifies helper data for 
      walking kernel callback frames.


### -field StackFrameSize

Set to <code>sizeof(STACKFRAME_EX)</code>.


### -field InlineFrameContext

Specifies the type of the inline frame context.



#### INLINE_FRAME_CONTEXT_INIT (0)



#### INLINE_FRAME_CONTEXT_IGNORE (0xffffffff)

