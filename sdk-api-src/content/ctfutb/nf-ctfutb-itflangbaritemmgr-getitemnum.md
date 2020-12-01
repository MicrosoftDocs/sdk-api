---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItemNum
title: ITfLangBarItemMgr::GetItemNum (ctfutb.h)
description: ITfLangBarItemMgr::GetItemNum method
helpviewer_keywords: ["GetItemNum","GetItemNum method [Text Services Framework]","GetItemNum method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","GetItemNum method","ITfLangBarItemMgr.GetItemNum","ITfLangBarItemMgr::GetItemNum","_tsf_itflangbaritemmgr_getitemnum_ref","ctfutb/ITfLangBarItemMgr::GetItemNum","tsf.itflangbaritemmgr_getitemnum"]
old-location: tsf\itflangbaritemmgr_getitemnum.htm
tech.root: TSF
ms.assetid: 0caf54b1-f862-4fc2-b593-c0e9f60d71cc
ms.date: 12/05/2018
ms.keywords: GetItemNum, GetItemNum method [Text Services Framework], GetItemNum method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItemNum method, ITfLangBarItemMgr.GetItemNum, ITfLangBarItemMgr::GetItemNum, _tsf_itflangbaritemmgr_getitemnum_ref, ctfutb/ITfLangBarItemMgr::GetItemNum, tsf.itflangbaritemmgr_getitemnum
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
 - ITfLangBarItemMgr::GetItemNum
 - ctfutb/ITfLangBarItemMgr::GetItemNum
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
 - ITfLangBarItemMgr.GetItemNum
---

# ITfLangBarItemMgr::GetItemNum


## -description

Obtains the number of items in the language bar.

## -parameters

### -param pulCount [out]

Pointer to a <b>ULONG</b> that receives the number of items in the language bar.

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
<i>pulCount</i> is invalid.

</td>
</tr>
</table>

