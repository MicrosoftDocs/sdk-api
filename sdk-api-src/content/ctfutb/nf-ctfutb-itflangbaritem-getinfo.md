---
UID: NF:ctfutb.ITfLangBarItem.GetInfo
title: ITfLangBarItem::GetInfo (ctfutb.h)
description: ITfLangBarItem::GetInfo method
helpviewer_keywords: ["GetInfo","GetInfo method [Text Services Framework]","GetInfo method [Text Services Framework]","ITfLangBarItem interface","ITfLangBarItem interface [Text Services Framework]","GetInfo method","ITfLangBarItem.GetInfo","ITfLangBarItem::GetInfo","_tsf_itflangbaritem_getinfo_ref","ctfutb/ITfLangBarItem::GetInfo","tsf.itflangbaritem_getinfo"]
old-location: tsf\itflangbaritem_getinfo.htm
tech.root: TSF
ms.assetid: b32e433a-c0d6-418e-bf11-2291c85373c2
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [Text Services Framework], GetInfo method [Text Services Framework],ITfLangBarItem interface, ITfLangBarItem interface [Text Services Framework],GetInfo method, ITfLangBarItem.GetInfo, ITfLangBarItem::GetInfo, _tsf_itflangbaritem_getinfo_ref, ctfutb/ITfLangBarItem::GetInfo, tsf.itflangbaritem_getinfo
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
 - ITfLangBarItem::GetInfo
 - ctfutb/ITfLangBarItem::GetInfo
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
 - ITfLangBarItem.GetInfo
---

# ITfLangBarItem::GetInfo


## -description

Obtains information about the language bar item.

## -parameters

### -param pInfo [out]

Pointer to a <a href="/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo">TF_LANGBARITEMINFO</a> structure that receives the language bar item information.

Starting with Windows 8, the item will be ignored if the structure does not include GUID_LBI_INPUTMODE. For more information, see [Third-party input method editors](https://docs.microsoft.com/en-us/windows/win32/w8cookbook/third-party-input-method-editors#manifestation) in the Compatibility cookbook for Windows.

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
<i>pInfo</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>

<a href="/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo">TF_LANGBARITEMINFO</a>
