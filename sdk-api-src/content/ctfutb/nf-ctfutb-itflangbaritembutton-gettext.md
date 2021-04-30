---
UID: NF:ctfutb.ITfLangBarItemButton.GetText
title: ITfLangBarItemButton::GetText (ctfutb.h)
description: ITfLangBarItemButton::GetText method
helpviewer_keywords: ["GetText","GetText method [Text Services Framework]","GetText method [Text Services Framework]","ITfLangBarItemButton interface","ITfLangBarItemButton interface [Text Services Framework]","GetText method","ITfLangBarItemButton.GetText","ITfLangBarItemButton::GetText","_tsf_itflangbaritembutton_gettext_ref","ctfutb/ITfLangBarItemButton::GetText","tsf.itflangbaritembutton_gettext"]
old-location: tsf\itflangbaritembutton_gettext.htm
tech.root: TSF
ms.assetid: 9c50f934-d968-4a3d-8455-8923d98b926e
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Text Services Framework], GetText method [Text Services Framework],ITfLangBarItemButton interface, ITfLangBarItemButton interface [Text Services Framework],GetText method, ITfLangBarItemButton.GetText, ITfLangBarItemButton::GetText, _tsf_itflangbaritembutton_gettext_ref, ctfutb/ITfLangBarItemButton::GetText, tsf.itflangbaritembutton_gettext
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
 - ITfLangBarItemButton::GetText
 - ctfutb/ITfLangBarItemButton::GetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemButton.GetText
---

# ITfLangBarItemButton::GetText


## -description

Obtains the text to be displayed for the button in the language bar.

## -parameters

### -param pbstrText [out]

Pointer to a <b>BSTR</b> that receives the string for the language bar item. This string must be allocated using the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> function. The caller must free this buffer when it is no longer required by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstrText</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembutton">ITfLangBarItemButton</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>