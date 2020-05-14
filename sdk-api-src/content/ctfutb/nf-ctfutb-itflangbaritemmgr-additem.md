---
UID: NF:ctfutb.ITfLangBarItemMgr.AddItem
title: ITfLangBarItemMgr::AddItem (ctfutb.h)
description: ITfLangBarItemMgr::AddItem methodhelpviewer_keywords: ["AddItem","AddItem method [Text Services Framework]","AddItem method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","AddItem method","ITfLangBarItemMgr.AddItem","ITfLangBarItemMgr::AddItem","_tsf_itflangbaritemmgr_additem_ref","ctfutb/ITfLangBarItemMgr::AddItem","tsf.itflangbaritemmgr_additem"]
old-location: tsf\itflangbaritemmgr_additem.htm
tech.root: TSF
ms.assetid: c9a36b2c-e7ea-4932-928e-05dd05ca02ca
ms.date: 12/05/2018
ms.keywords: AddItem, AddItem method [Text Services Framework], AddItem method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AddItem method, ITfLangBarItemMgr.AddItem, ITfLangBarItemMgr::AddItem, _tsf_itflangbaritemmgr_additem_ref, ctfutb/ITfLangBarItemMgr::AddItem, tsf.itflangbaritemmgr_additem
f1_keywords:
- ctfutb/ITfLangBarItemMgr.AddItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfLangBarItemMgr.AddItem
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarItemMgr::AddItem


## -description

Adds an item to the language bar.

## -parameters




### -param punk [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object to add to the language bar.


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
<i>punk</i> is invalid.

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




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>
 

 

