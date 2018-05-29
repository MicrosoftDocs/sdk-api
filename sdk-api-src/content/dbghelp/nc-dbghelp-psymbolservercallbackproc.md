---
UID: NC:dbghelp.PSYMBOLSERVERCALLBACKPROC
title: PSYMBOLSERVERCALLBACKPROC
author: windows-sdk-content
description: An entry point to the symbol server DLL.
old-location: winprog\symbolservercallback.htm
old-project: DevNotes
ms.assetid: 11c833ee-a9f3-4d08-a6cd-0da62844c589
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PSYMBOLSERVERCALLBACKPROC, SSRVACTION_EVENT, SSRVACTION_QUERYCANCEL, SSRVACTION_SIZE, SSRVACTION_TRACE, SymbolServerCallback, SymbolServerCallback callback, SymbolServerCallback callback function [Windows API], _win32_symbolservercallback, base.symbolservercallback, dbghelp/SymbolServerCallback, winprog.symbolservercallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	DbgHelp.h
api_name:
-	SymbolServerCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
Provide debug trace information. The <i>data</i> parameter is a pointer to an <a href="https://msdn.microsoft.com/1d63007a-7542-4626-99a5-41461e00dbb4">IMAGEHLP_CBA_EVENT</a> structure.

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

The context information provided by calling <a href="https://msdn.microsoft.com/279181a6-60b7-40e3-b801-4b8674d93478">SymbolServerSetOptions</a> with SSRVOPT_SETCONTEXT.


## -returns



To indicate success, return <b>TRUE</b>.

To indicate failure, return <b>FALSE</b> and call the 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function to indicate an error condition. If you do not handle a particular action code, you should also return <b>FALSE</b>. (Returning <b>TRUE</b> in this case may have unintended consequences.)




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp
		  Functions</a>



<a href="https://msdn.microsoft.com/1d63007a-7542-4626-99a5-41461e00dbb4">IMAGEHLP_CBA_EVENT</a>
 

 

