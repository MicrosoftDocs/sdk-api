---
UID: NC:dbghelp.PSYMBOLSERVERCALLBACKPROC
title: PSYMBOLSERVERCALLBACKPROC (dbghelp.h)
description: An entry point to the symbol server DLL.
helpviewer_keywords: ["PSYMBOLSERVERCALLBACKPROC","SSRVACTION_EVENT","SSRVACTION_QUERYCANCEL","SSRVACTION_SIZE","SSRVACTION_TRACE","SymbolServerCallback","SymbolServerCallback callback","SymbolServerCallback callback function [Windows API]","_win32_symbolservercallback","base.symbolservercallback","dbghelp/SymbolServerCallback","winprog.symbolservercallback"]
old-location: winprog\symbolservercallback.htm
tech.root: winprog
ms.assetid: 11c833ee-a9f3-4d08-a6cd-0da62844c589
ms.date: 12/05/2018
ms.keywords: PSYMBOLSERVERCALLBACKPROC, SSRVACTION_EVENT, SSRVACTION_QUERYCANCEL, SSRVACTION_SIZE, SSRVACTION_TRACE, SymbolServerCallback, SymbolServerCallback callback, SymbolServerCallback callback function [Windows API], _win32_symbolservercallback, base.symbolservercallback, dbghelp/SymbolServerCallback, winprog.symbolservercallback
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
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PSYMBOLSERVERCALLBACKPROC
 - dbghelp/PSYMBOLSERVERCALLBACKPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymbolServerCallback
---

# PSYMBOLSERVERCALLBACKPROC callback function


## -description

An entry point to the symbol server DLL.

The <b>PSYMBOLSERVERCALLBACKPROC</b> type defines a pointer to this callback function. 
<i>SymbolServerCallback</i> is a placeholder for the library-defined function name.

## -parameters

### -param action [in]

The action code. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSRVACTION_EVENT"></a><a id="ssrvaction_event"></a><dl>
<dt><b>SSRVACTION_EVENT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Provide debug trace information. The <i>data</i> parameter is a pointer to an <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_event">IMAGEHLP_CBA_EVENT</a> structure.

<b>DbgHelp 6.0 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SSRVACTION_QUERYCANCEL"></a><a id="ssrvaction_querycancel"></a><dl>
<dt><b>SSRVACTION_QUERYCANCEL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Cancel the file copy. The <i>data</i> parameter is a <b>ULONG64</b> value. If this value is zero, continue the operation. Otherwise, cancel the operation.

<b>DbgHelp 6.0 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SSRVACTION_SIZE"></a><a id="ssrvaction_size"></a><dl>
<dt><b>SSRVACTION_SIZE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
 The <i>data</i> parameter is the size of the file to be provided by the system.

</td>
</tr>
<tr>
<td width="40%"><a id="SSRVACTION_TRACE"></a><a id="ssrvaction_trace"></a><dl>
<dt><b>SSRVACTION_TRACE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Provide debug trace information. The <i>data</i> parameter is a text string.

</td>
</tr>
</table>

### -param data [in]

The format of this parameter depends on the value of the <i>action</i> parameter.

### -param context [in]

The context information provided by calling <a href="/previous-versions/ff797954(v=vs.85)">SymbolServerSetOptions</a> with SSRVOPT_SETCONTEXT.

## -returns

To indicate success, return <b>TRUE</b>.

To indicate failure, return <b>FALSE</b> and call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function to indicate an error condition. If you do not handle a particular action code, you should also return <b>FALSE</b>. (Returning <b>TRUE</b> in this case may have unintended consequences.)

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp
		  Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_event">IMAGEHLP_CBA_EVENT</a>