---
UID: NF:ctfutb.ITfSystemLangBarItemText.GetItemText
title: ITfSystemLangBarItemText::GetItemText (ctfutb.h)
description: The ITfSystemLangBarItemText::GetItemText method obtains the text displayed for the system language bar menu.
helpviewer_keywords: ["GetItemText","GetItemText method [Text Services Framework]","GetItemText method [Text Services Framework]","ITfSystemLangBarItemText interface","ITfSystemLangBarItemText interface [Text Services Framework]","GetItemText method","ITfSystemLangBarItemText.GetItemText","ITfSystemLangBarItemText::GetItemText","ctfutb/ITfSystemLangBarItemText::GetItemText","tsf.itfsystemlangbaritemtext_getitemtext"]
old-location: tsf\itfsystemlangbaritemtext_getitemtext.htm
tech.root: TSF
ms.assetid: eec4486e-c4fd-484f-bbd7-9f2ee974459b
ms.date: 12/05/2018
ms.keywords: GetItemText, GetItemText method [Text Services Framework], GetItemText method [Text Services Framework],ITfSystemLangBarItemText interface, ITfSystemLangBarItemText interface [Text Services Framework],GetItemText method, ITfSystemLangBarItemText.GetItemText, ITfSystemLangBarItemText::GetItemText, ctfutb/ITfSystemLangBarItemText::GetItemText, tsf.itfsystemlangbaritemtext_getitemtext
req.header: ctfutb.h
req.include-header: Msctf.h
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
 - ITfSystemLangBarItemText::GetItemText
 - ctfutb/ITfSystemLangBarItemText::GetItemText
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
 - ITfSystemLangBarItemText.GetItemText
---

# ITfSystemLangBarItemText::GetItemText


## -description

The <b>ITfSystemLangBarItemText::GetItemText</b> method obtains the text displayed for the system language bar menu.

## -parameters

### -param pbstrText [out]

[out] A pointer to BSTR that contains the current description.

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
A parameter is invalid.

</td>
</tr>
</table>

