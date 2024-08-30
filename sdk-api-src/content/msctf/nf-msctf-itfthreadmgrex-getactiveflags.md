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

| Value | Meaning |
|:-----------------------------------|:-----------------------------------|
| <span id="TF_TMF_NOACTIVATETIP"></span><span id="tf_tmf_noactivatetip"></span> **TF_TMF_NOACTIVATETIP** | TSF was activated with the TF_TMAE_NOACTIVATETIP flag. |
| <span id="TF_TMF_SECUREMODE"></span><span id="tf_tmf_securemode"></span> **TF_TMF_SECUREMODE** | TSF is running as secure mode. |
| <span id="TF_TMF_UIELEMENTENABLEDONLY"></span><span id="tf_tmf_uielementenabledonly"></span> **TF_TMF_UIELEMENTENABLEDONLY** | TSF is running with text services that support only UIElement. |
| <span id="TF_TMF_COMLESS"></span><span id="tf_tmf_comless"></span> **TF_TMF_COMLESS** | TSF is running without COM. |
| <span id="TF_TMF_WOW16"></span><span id="tf_tmf_wow16"></span> **TF_TMF_WOW16** | TSF is running in 16bit task. |
| <span id="TF_TMF_CONSOLE"></span><span id="tf_tmf_console"></span> **TF_TMF_CONSOLE** | TSF is running for console. |
| <span id="TF_TMF_IMMERSIVEMODE"></span><span id="tf_tmf_immersivemode"></span> **TF_TMF_IMMERSIVEMODE** | **Starting with Windows 8:** TSF is active in a Windows Store app. |
| <span id="TF_TMF_ACTIVATED"></span><span id="tf_tmf_activated"></span> **TF_TMF_ACTIVATED** | TSF is active. |

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

