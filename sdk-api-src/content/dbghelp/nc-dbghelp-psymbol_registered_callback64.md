---
UID: NC:dbghelp.PSYMBOL_REGISTERED_CALLBACK64
title: PSYMBOL_REGISTERED_CALLBACK64 (dbghelp.h)
description: PSYMBOL_REGISTERED_CALLBACK64 (dbghelp.h) is an application-defined callback function used with the SymRegisterCallback64 function.
helpviewer_keywords: ["CBA_DEBUG_INFO","CBA_DEFERRED_SYMBOL_LOAD_CANCEL","CBA_DEFERRED_SYMBOL_LOAD_COMPLETE","CBA_DEFERRED_SYMBOL_LOAD_FAILURE","CBA_DEFERRED_SYMBOL_LOAD_PARTIAL","CBA_DEFERRED_SYMBOL_LOAD_START","CBA_DUPLICATE_SYMBOL","CBA_EVENT","CBA_READ_MEMORY","CBA_SET_OPTIONS","CBA_SRCSRV_EVENT","CBA_SRCSRV_INFO","CBA_SYMBOLS_UNLOADED","PSYMBOL_REGISTERED_CALLBACK","PSYMBOL_REGISTERED_CALLBACK64","SymRegisterCallbackProc64","SymRegisterCallbackProc64 callback","SymRegisterCallbackProc64 callback function","_win32_symregistercallbackproc64","base.symregistercallbackproc64","dbghelp/SymRegisterCallbackProc64"]
old-location: base\symregistercallbackproc64.htm
tech.root: Debug
ms.assetid: f3ba952b-ecc5-4235-a806-00c82d40e611
ms.date: 08/04/2022
ms.keywords: CBA_DEBUG_INFO, CBA_DEFERRED_SYMBOL_LOAD_CANCEL, CBA_DEFERRED_SYMBOL_LOAD_COMPLETE, CBA_DEFERRED_SYMBOL_LOAD_FAILURE, CBA_DEFERRED_SYMBOL_LOAD_PARTIAL, CBA_DEFERRED_SYMBOL_LOAD_START, CBA_DUPLICATE_SYMBOL, CBA_EVENT, CBA_READ_MEMORY, CBA_SET_OPTIONS, CBA_SRCSRV_EVENT, CBA_SRCSRV_INFO, CBA_SYMBOLS_UNLOADED, PSYMBOL_REGISTERED_CALLBACK, PSYMBOL_REGISTERED_CALLBACK64, SymRegisterCallbackProc64, SymRegisterCallbackProc64 callback, SymRegisterCallbackProc64 callback function, _win32_symregistercallbackproc64, base.symregistercallbackproc64, dbghelp/SymRegisterCallbackProc64
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
 - PSYMBOL_REGISTERED_CALLBACK64
 - dbghelp/PSYMBOL_REGISTERED_CALLBACK64
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
 - SymRegisterCallbackProc64
---

# PSYMBOL_REGISTERED_CALLBACK64 callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregistercallback">SymRegisterCallback64</a> function. It is called by the symbol handler.

The <b>PSYMBOL_REGISTERED_CALLBACK64</b> type defines a pointer to this callback function. 
<b>SymRegisterCallbackProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param ActionCode [in]

The callback code. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CBA_DEBUG_INFO"></a><a id="cba_debug_info"></a><dl>
<dt><b>CBA_DEBUG_INFO</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Display verbose information.

The <i>CallbackData</i> parameter is a pointer to a string.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DEFERRED_SYMBOL_LOAD_CANCEL"></a><a id="cba_deferred_symbol_load_cancel"></a><dl>
<dt><b>CBA_DEFERRED_SYMBOL_LOAD_CANCEL</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Deferred symbol loading has started. To cancel the symbol load, return <b>TRUE</b>. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DEFERRED_SYMBOL_LOAD_COMPLETE"></a><a id="cba_deferred_symbol_load_complete"></a><dl>
<dt><b>CBA_DEFERRED_SYMBOL_LOAD_COMPLETE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Deferred symbol load has completed. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DEFERRED_SYMBOL_LOAD_FAILURE"></a><a id="cba_deferred_symbol_load_failure"></a><dl>
<dt><b>CBA_DEFERRED_SYMBOL_LOAD_FAILURE</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Deferred symbol load has failed. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a> structure. The symbol handler will attempt to load the symbols again if the callback function sets the <b>FileName</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DEFERRED_SYMBOL_LOAD_PARTIAL"></a><a id="cba_deferred_symbol_load_partial"></a><dl>
<dt><b>CBA_DEFERRED_SYMBOL_LOAD_PARTIAL</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Deferred symbol load has partially completed. The symbol loader is unable to read the image header from either the image file or the specified module.

The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a> structure. The symbol handler will attempt to load the symbols again if the callback function sets the <b>FileName</b> member of this structure.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DEFERRED_SYMBOL_LOAD_START"></a><a id="cba_deferred_symbol_load_start"></a><dl>
<dt><b>CBA_DEFERRED_SYMBOL_LOAD_START</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Deferred symbol load has started. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_DUPLICATE_SYMBOL"></a><a id="cba_duplicate_symbol"></a><dl>
<dt><b>CBA_DUPLICATE_SYMBOL</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Duplicate symbols were found. This reason is used only in COFF or CodeView format. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_duplicate_symbol">IMAGEHLP_DUPLICATE_SYMBOL64</a> structure. To specify which symbol to use, set the <b>SelectedSymbol</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_EVENT"></a><a id="cba_event"></a><dl>
<dt><b>CBA_EVENT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Display verbose information. If you do not handle this event, the information is resent through the CBA_DEBUG_INFO event.

The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_event">IMAGEHLP_CBA_EVENT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_READ_MEMORY"></a><a id="cba_read_memory"></a><dl>
<dt><b>CBA_READ_MEMORY</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
The loaded image has been read. 




The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_read_memory">IMAGEHLP_CBA_READ_MEMORY</a> structure. The callback function should read the number of bytes specified by the <b>bytes</b> member into the buffer specified by the <b>buf</b> member, and update the <b>bytesread</b> member accordingly. 

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_SET_OPTIONS"></a><a id="cba_set_options"></a><dl>
<dt><b>CBA_SET_OPTIONS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Symbol options have been updated. To retrieve the current options, call the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetoptions">SymGetOptions</a> function. 




The <i>CallbackData</i> parameter should be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_SRCSRV_EVENT"></a><a id="cba_srcsrv_event"></a><dl>
<dt><b>CBA_SRCSRV_EVENT</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Display verbose information for source server. If you do not handle this event, the information is resent through the CBA_DEBUG_INFO event.

The <i>CallbackData</i> parameter is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_event">IMAGEHLP_CBA_EVENT</a> structure.

<b>DbgHelp 6.6 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_SRCSRV_INFO"></a><a id="cba_srcsrv_info"></a><dl>
<dt><b>CBA_SRCSRV_INFO</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Display verbose information for source server.

The <i>CallbackData</i> parameter is a pointer to a string.

<b>DbgHelp 6.6 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CBA_SYMBOLS_UNLOADED"></a><a id="cba_symbols_unloaded"></a><dl>
<dt><b>CBA_SYMBOLS_UNLOADED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Symbols have been unloaded. 




The <i>CallbackData</i> parameter should be ignored.

</td>
</tr>
</table>

### -param CallbackData [in, optional]

Data for the operation. The format of this data depends on the value of the <i>ActionCode</i> parameter.

If the callback function was registered with <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregistercallback">SymRegisterCallbackW64</a>, the data is a Unicode string or data structure. Otherwise, the data uses ANSI format.

### -param UserContext [in, optional]

User-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregistercallback">SymRegisterCallback64</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some context.

## -returns

To indicate success handling the code, return <b>TRUE</b>.

To indicate failure handling the code, return <b>FALSE</b>. If your code does not handle a particular code, you should also return <b>FALSE</b>. (Returning <b>TRUE</b> in this case may have unintended consequences.)

## -remarks

The calling application gets called through the registered callback function as a result of another call to one of the symbol handler functions. The calling application must be prepared for the possible side effects that this can cause. If the application has only one callback function that is being used by multiple threads, then care may be necessary to synchronize some types of data access while in the context of the callback function.

This callback function supersedes the <i>PSYMBOL_REGISTERED_CALLBACK</i> callback function.  <i>PSYMBOL_REGISTERED_CALLBACK</i> is defined as follows in Dbghelp.h.


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PSYMBOL_REGISTERED_CALLBACK PSYMBOL_REGISTERED_CALLBACK64
#else
typedef BOOL
(CALLBACK *PSYMBOL_REGISTERED_CALLBACK)(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt PVOID CallbackData,
    __in_opt PVOID UserContext
    );
#endif
```


For a more extensive example, read <a href="/windows/desktop/Debug/getting-notifications">Getting Notifications</a>.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/Debug/getting-notifications">Getting Notifications</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_event">IMAGEHLP_CBA_EVENT</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_cba_read_memory">IMAGEHLP_CBA_READ_MEMORY</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_deferred_symbol_load">IMAGEHLP_DEFERRED_SYMBOL_LOAD64</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_duplicate_symbol">IMAGEHLP_DUPLICATE_SYMBOL64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregistercallback">SymRegisterCallback64</a>
