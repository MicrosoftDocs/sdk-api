---
UID: NF:msctf.ITfThreadMgrEx.GetActiveFlags
title: ITfThreadMgrEx::GetActiveFlags (msctf.h)
description: The ITfThreadMgrEx::GetActiveFlags method returns the flags TSF is active with.
helpviewer_keywords: ["GetActiveFlags","GetActiveFlags method [Text Services Framework]","GetActiveFlags method [Text Services Framework]","ITfThreadMgrEx interface","ITfThreadMgrEx interface [Text Services Framework]","GetActiveFlags method","ITfThreadMgrEx.GetActiveFlags","ITfThreadMgrEx::GetActiveFlags","TF_TMF_ACTIVATED","TF_TMF_COMLESS","TF_TMF_CONSOLE","TF_TMF_NOACTIVATETIP","TF_TMF_SECUREMODE","TF_TMF_UIELEMENTENABLEDONLY","TF_TMF_WOW16","msctf/ITfThreadMgrEx::GetActiveFlags","tsf.itfthreadmgrex_getactiveflags"]
old-location: tsf\itfthreadmgrex_getactiveflags.htm
tech.root: TSF
ms.assetid: 2b15ddc3-0719-48cf-95fc-9c6d1e15fd4f
ms.date: 12/05/2018
ms.keywords: GetActiveFlags, GetActiveFlags method [Text Services Framework], GetActiveFlags method [Text Services Framework],ITfThreadMgrEx interface, ITfThreadMgrEx interface [Text Services Framework],GetActiveFlags method, ITfThreadMgrEx.GetActiveFlags, ITfThreadMgrEx::GetActiveFlags, TF_TMF_ACTIVATED, TF_TMF_COMLESS, TF_TMF_CONSOLE, TF_TMF_NOACTIVATETIP, TF_TMF_SECUREMODE, TF_TMF_UIELEMENTENABLEDONLY, TF_TMF_WOW16, msctf/ITfThreadMgrEx::GetActiveFlags, tsf.itfthreadmgrex_getactiveflags
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgrEx::GetActiveFlags
 - msctf/ITfThreadMgrEx::GetActiveFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfThreadMgrEx.GetActiveFlags
---

# ITfThreadMgrEx::GetActiveFlags


## -description

The <b>ITfThreadMgrEx::GetActiveFlags</b> method returns the flags TSF is active with.

## -parameters

### -param lpdwFlags [out]

The pointer to the DWORD value to receives the active flags of TSF.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_NOACTIVATETIP"></a><a id="tf_tmf_noactivatetip"></a><dl>
<dt><b>TF_TMF_NOACTIVATETIP</b></dt>
</dl>
</td>
<td width="60%">
TSF was activated with the TF_TMAE_NOACTIVATETIP flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_SECUREMODE"></a><a id="tf_tmf_securemode"></a><dl>
<dt><b>TF_TMF_SECUREMODE</b></dt>
</dl>
</td>
<td width="60%">
TSF is running as secure mode.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_UIELEMENTENABLEDONLY"></a><a id="tf_tmf_uielementenabledonly"></a><dl>
<dt><b>TF_TMF_UIELEMENTENABLEDONLY</b></dt>
</dl>
</td>
<td width="60%">
TSF is running with text services that support only UIElement.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_COMLESS"></a><a id="tf_tmf_comless"></a><dl>
<dt><b>TF_TMF_COMLESS</b></dt>
</dl>
</td>
<td width="60%">
TSF is running without COM.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_WOW16"></a><a id="tf_tmf_wow16"></a><dl>
<dt><b>TF_TMF_WOW16</b></dt>
</dl>
</td>
<td width="60%">
TSF is running in 16bit task.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_CONSOLE"></a><a id="tf_tmf_console"></a><dl>
<dt><b>TF_TMF_CONSOLE</b></dt>
</dl>
</td>
<td width="60%">
TSF is running for console.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_ACTIVATED"></a><a id="tf_tmf_activated"></a><dl>
<dt><b>TF_TMF_ACTIVATED</b></dt>
</dl>
</td>
<td width="60%">
TSF is active.

</td>
</tr>
</table>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

