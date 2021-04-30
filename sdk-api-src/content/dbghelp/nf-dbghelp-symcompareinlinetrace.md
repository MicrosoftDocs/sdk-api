---
UID: NF:dbghelp.SymCompareInlineTrace
title: SymCompareInlineTrace function (dbghelp.h)
description: Compares two inline traces.
helpviewer_keywords: ["SymCompareInlineTrace","SymCompareInlineTrace function","base.symcompareinlinetrace","dbghelp/SymCompareInlineTrace"]
old-location: base\symcompareinlinetrace.htm
tech.root: Debug
ms.assetid: 24daca16-834c-424a-8569-e448f515d76f
ms.date: 12/05/2018
ms.keywords: SymCompareInlineTrace, SymCompareInlineTrace function, base.symcompareinlinetrace, dbghelp/SymCompareInlineTrace
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
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymCompareInlineTrace
 - dbghelp/SymCompareInlineTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymCompareInlineTrace
---

# SymCompareInlineTrace function


## -description

Compares two inline traces.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Address1 [in]

The first address to be compared.

### -param InlineContext1 [in]

The inline context for the first trace to be compared.

### -param RetAddress1 [in]

The return address of the first trace to be compared.

### -param Address2 [in]

The second address to be compared.

### -param RetAddress2 [in]

The return address of the second trace to be compared.

## -returns

Indicates the result of the comparison.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_ERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_IDENTICAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The inline contexts are identical.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPIN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-in of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPOUT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-out of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPOVER</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-over of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_DIFFERENT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The inline contexts are different.

</td>
</tr>
</table>