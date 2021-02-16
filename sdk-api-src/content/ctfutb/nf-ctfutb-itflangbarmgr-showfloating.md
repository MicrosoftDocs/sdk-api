---
UID: NF:ctfutb.ITfLangBarMgr.ShowFloating
title: ITfLangBarMgr::ShowFloating (ctfutb.h)
description: ITfLangBarMgr::ShowFloating method
helpviewer_keywords: ["ITfLangBarMgr interface [Text Services Framework]","ShowFloating method","ITfLangBarMgr.ShowFloating","ITfLangBarMgr::ShowFloating","ShowFloating","ShowFloating method [Text Services Framework]","ShowFloating method [Text Services Framework]","ITfLangBarMgr interface","TF_SFT_DESKBAND","TF_SFT_DOCK","TF_SFT_EXTRAICONSONMINIMIZED","TF_SFT_HIDDEN","TF_SFT_HIGHTRANSPARENCY","TF_SFT_LABELS","TF_SFT_LOWTRANSPARENCY","TF_SFT_MINIMIZED","TF_SFT_NOEXTRAICONSONMINIMIZED","TF_SFT_NOLABELS","TF_SFT_NOTRANSPARENCY","TF_SFT_SHOWNORMAL","_tsf_itflangbarmgr_showfloating_ref","ctfutb/ITfLangBarMgr::ShowFloating","tsf.itflangbarmgr_showfloating"]
old-location: tsf\itflangbarmgr_showfloating.htm
tech.root: TSF
ms.assetid: f49987c7-476d-4add-9d43-83de78693420
ms.date: 12/05/2018
ms.keywords: ITfLangBarMgr interface [Text Services Framework],ShowFloating method, ITfLangBarMgr.ShowFloating, ITfLangBarMgr::ShowFloating, ShowFloating, ShowFloating method [Text Services Framework], ShowFloating method [Text Services Framework],ITfLangBarMgr interface, TF_SFT_DESKBAND, TF_SFT_DOCK, TF_SFT_EXTRAICONSONMINIMIZED, TF_SFT_HIDDEN, TF_SFT_HIGHTRANSPARENCY, TF_SFT_LABELS, TF_SFT_LOWTRANSPARENCY, TF_SFT_MINIMIZED, TF_SFT_NOEXTRAICONSONMINIMIZED, TF_SFT_NOLABELS, TF_SFT_NOTRANSPARENCY, TF_SFT_SHOWNORMAL, _tsf_itflangbarmgr_showfloating_ref, ctfutb/ITfLangBarMgr::ShowFloating, tsf.itflangbarmgr_showfloating
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - ITfLangBarMgr::ShowFloating
 - ctfutb/ITfLangBarMgr::ShowFloating
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
 - ITfLangBarMgr.ShowFloating
---

# ITfLangBarMgr::ShowFloating


## -description

Configures display settings for the floating language bar.

## -parameters

### -param dwFlags [in]

Specifies language bar display settings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_SHOWNORMAL"></a><a id="tf_sft_shownormal"></a><dl>
<dt><b>TF_SFT_SHOWNORMAL</b></dt>
</dl>
</td>
<td width="60%">
Display the language bar as a floating window. This constant cannot be combined with the TF_SFT_DOCK, TF_SFT_MINIMIZED, TF_SFT_HIDDEN, or TF_SFT_DESKBAND constants.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_DOCK"></a><a id="tf_sft_dock"></a><dl>
<dt><b>TF_SFT_DOCK</b></dt>
</dl>
</td>
<td width="60%">
Deprecated as of Windows Vista. Dock the language bar in its own task pane. This constant cannot be combined with the TF_SFT_SHOWNORMAL, TF_SFT_MINIMIZED, TF_SFT_HIDDEN, or TF_SFT_DESKBAND constants. Available only on Windows XP.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_MINIMIZED"></a><a id="tf_sft_minimized"></a><dl>
<dt><b>TF_SFT_MINIMIZED</b></dt>
</dl>
</td>
<td width="60%">
Deprecated as of Windows Vista. Display the language bar as a single icon in the system tray. This constant cannot be combined with the TF_SFT_SHOWNORMAL, TF_SFT_DOCK, TF_SFT_HIDDEN, or TF_SFT_DESKBAND constants.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_HIDDEN"></a><a id="tf_sft_hidden"></a><dl>
<dt><b>TF_SFT_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
Hide the language bar. This constant cannot be combined with the TF_SFT_SHOWNORMAL, TF_SFT_DOCK, TF_SFT_MINIMIZED, or TF_SFT_DESKBAND constants.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_NOTRANSPARENCY"></a><a id="tf_sft_notransparency"></a><dl>
<dt><b>TF_SFT_NOTRANSPARENCY</b></dt>
</dl>
</td>
<td width="60%">
Make the language bar opaque.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_LOWTRANSPARENCY"></a><a id="tf_sft_lowtransparency"></a><dl>
<dt><b>TF_SFT_LOWTRANSPARENCY</b></dt>
</dl>
</td>
<td width="60%">
Make the language bar partially transparent. Available only on Windows 2000 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_HIGHTRANSPARENCY"></a><a id="tf_sft_hightransparency"></a><dl>
<dt><b>TF_SFT_HIGHTRANSPARENCY</b></dt>
</dl>
</td>
<td width="60%">
Make the language bar highly transparent. Available only on Windows 2000 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_LABELS"></a><a id="tf_sft_labels"></a><dl>
<dt><b>TF_SFT_LABELS</b></dt>
</dl>
</td>
<td width="60%">
Display text labels next to language bar icons.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_NOLABELS"></a><a id="tf_sft_nolabels"></a><dl>
<dt><b>TF_SFT_NOLABELS</b></dt>
</dl>
</td>
<td width="60%">
Hide language bar icon text labels.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_EXTRAICONSONMINIMIZED"></a><a id="tf_sft_extraiconsonminimized"></a><dl>
<dt><b>TF_SFT_EXTRAICONSONMINIMIZED</b></dt>
</dl>
</td>
<td width="60%">
Display text service icons on the taskbar when the language bar is minimized.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_NOEXTRAICONSONMINIMIZED"></a><a id="tf_sft_noextraiconsonminimized"></a><dl>
<dt><b>TF_SFT_NOEXTRAICONSONMINIMIZED</b></dt>
</dl>
</td>
<td width="60%">
Hide text service icons on the taskbar when the language bar is minimized.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_SFT_DESKBAND"></a><a id="tf_sft_deskband"></a><dl>
<dt><b>TF_SFT_DESKBAND</b></dt>
</dl>
</td>
<td width="60%">
Dock the language bar in the system task bar. This constant cannot be combined with the TF_SFT_SHOWNORMAL, TF_SFT_DOCK, TF_SFT_MINIMIZED, or TF_SFT_HIDDEN constants. Available only on Windows XP.

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
<i>dwFlags</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr</a>



<a href="/windows/desktop/TSF/tf-sft--constants">TF_SFT_* Constants
      </a>