---
UID: NF:msctf.ITfThreadMgr2.GetActiveFlags
title: ITfThreadMgr2::GetActiveFlags (msctf.h)
description: Gets the active flags of the calling thread.
helpviewer_keywords: ["GetActiveFlags","GetActiveFlags method [Text Services Framework]","GetActiveFlags method [Text Services Framework]","ITfThreadMgr2 interface","ITfThreadMgr2 interface [Text Services Framework]","GetActiveFlags method","ITfThreadMgr2.GetActiveFlags","ITfThreadMgr2::GetActiveFlags","TF_TMF_ACTIVATED","TF_TMF_COMLESS","TF_TMF_CONSOLE","TF_TMF_IMMERSIVEMODE","TF_TMF_NOACTIVATETIP","TF_TMF_SECUREMODE","TF_TMF_UIELEMENTENABLEDONLY","TF_TMF_WOW16","msctf/ITfThreadMgr2::GetActiveFlags","tsf.itfthreadmgr2_getactiveflags"]
old-location: tsf\itfthreadmgr2_getactiveflags.htm
tech.root: TSF
ms.assetid: F0777E69-C9E2-4E40-9CE0-56084D1C8A41
ms.date: 12/05/2018
ms.keywords: GetActiveFlags, GetActiveFlags method [Text Services Framework], GetActiveFlags method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],GetActiveFlags method, ITfThreadMgr2.GetActiveFlags, ITfThreadMgr2::GetActiveFlags, TF_TMF_ACTIVATED, TF_TMF_COMLESS, TF_TMF_CONSOLE, TF_TMF_IMMERSIVEMODE, TF_TMF_NOACTIVATETIP, TF_TMF_SECUREMODE, TF_TMF_UIELEMENTENABLEDONLY, TF_TMF_WOW16, msctf/ITfThreadMgr2::GetActiveFlags, tsf.itfthreadmgr2_getactiveflags
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr2::GetActiveFlags
 - msctf/ITfThreadMgr2::GetActiveFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.GetActiveFlags
---

# ITfThreadMgr2::GetActiveFlags


## -description

Gets the active flags of the calling thread.

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

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>
