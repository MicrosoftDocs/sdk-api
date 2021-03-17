---
UID: NF:msctf.ITfThreadMgrEx.ActivateEx
title: ITfThreadMgrEx::ActivateEx (msctf.h)
description: The ITfThreadMgrEx::ActivateEx method is used by an application to initialize and activate TSF for the calling thread. Unlike ITfThreadMgr::Activate, ITfThreadMgrEx::ActivateEx can take a flag to specify how TSF is activated.
helpviewer_keywords: ["ActivateEx","ActivateEx method [Text Services Framework]","ActivateEx method [Text Services Framework]","ITfThreadMgrEx interface","ITfThreadMgrEx interface [Text Services Framework]","ActivateEx method","ITfThreadMgrEx.ActivateEx","ITfThreadMgrEx::ActivateEx","TF_TMAE_COMLESS","TF_TMAE_NOACTIVATEKEYBOARDLAYOUT","TF_TMAE_NOACTIVATETIP","TF_TMAE_SECUREMODE","TF_TMAE_UIELEMENTENABLEDONLY","msctf/ITfThreadMgrEx::ActivateEx","tsf.itfthreadmgrex_activateex"]
old-location: tsf\itfthreadmgrex_activateex.htm
tech.root: TSF
ms.assetid: a3cecc02-5228-4912-a609-f9f3334e11b7
ms.date: 12/05/2018
ms.keywords: ActivateEx, ActivateEx method [Text Services Framework], ActivateEx method [Text Services Framework],ITfThreadMgrEx interface, ITfThreadMgrEx interface [Text Services Framework],ActivateEx method, ITfThreadMgrEx.ActivateEx, ITfThreadMgrEx::ActivateEx, TF_TMAE_COMLESS, TF_TMAE_NOACTIVATEKEYBOARDLAYOUT, TF_TMAE_NOACTIVATETIP, TF_TMAE_SECUREMODE, TF_TMAE_UIELEMENTENABLEDONLY, msctf/ITfThreadMgrEx::ActivateEx, tsf.itfthreadmgrex_activateex
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
 - ITfThreadMgrEx::ActivateEx
 - msctf/ITfThreadMgrEx::ActivateEx
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
 - ITfThreadMgrEx.ActivateEx
---

# ITfThreadMgrEx::ActivateEx


## -description

The <b>ITfThreadMgrEx::ActivateEx</b> method is used by an application to initialize and activate TSF for the calling thread. Unlike <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate</a>, ITfThreadMgrEx::ActivateEx can take a flag to specify how TSF is activated.

## -parameters

### -param ptid [out]

[out] Pointer to a <a href="/windows/desktop/TSF/tfclientid">TfClientId</a> value that receives a client identifier.

### -param dwFlags [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_NOACTIVATETIP"></a><a id="tf_tmae_noactivatetip"></a><dl>
<dt><b>TF_TMAE_NOACTIVATETIP</b></dt>
</dl>
</td>
<td width="60%">
Text services will not be activated while ITfThreadMgrEx::ActivateEx is called. They will be activated when the calling thread has focus asynchronously.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_SECUREMODE"></a><a id="tf_tmae_securemode"></a><dl>
<dt><b>TF_TMAE_SECUREMODE</b></dt>
</dl>
</td>
<td width="60%">
TSF is activated in secure mode. Only text services that support the secure mode will be activated.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_UIELEMENTENABLEDONLY"></a><a id="tf_tmae_uielementenabledonly"></a><dl>
<dt><b>TF_TMAE_UIELEMENTENABLEDONLY</b></dt>
</dl>
</td>
<td width="60%">
TSF activates only text services that are categorized in GUID_TFCAT_TIPCAP_UIELEMENTENABLED.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_COMLESS"></a><a id="tf_tmae_comless"></a><dl>
<dt><b>TF_TMAE_COMLESS</b></dt>
</dl>
</td>
<td width="60%">
TSF does not use COM. TSF activate only text services that are categorized in GUID_TFCAT_TIPCAP_COMLESS.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_NOACTIVATEKEYBOARDLAYOUT"></a><a id="tf_tmae_noactivatekeyboardlayout"></a><dl>
<dt><b>TF_TMAE_NOACTIVATEKEYBOARDLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
TSF does not sync the current keyboard layout while ITfThreadMgrEx::ActivateEx() is called. The keyboard layout will be adjusted when the calling thread gets focus. This flag must be used with TF_TMAE_NOACTIVATETIP.

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

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgrex">ITfThreadMgrEx</a>