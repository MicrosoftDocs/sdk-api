---
UID: NF:ctfutb.ITfLangBarItemMgr.RemoveItem
title: ITfLangBarItemMgr::RemoveItem (ctfutb.h)
author: windows-sdk-content
description: ITfLangBarItemMgr::RemoveItem method
old-location: tsf\itflangbaritemmgr_removeitem.htm
tech.root: TSF
ms.assetid: 5a56a8f4-8011-4847-869f-c859ec90da3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],RemoveItem method, ITfLangBarItemMgr.RemoveItem, ITfLangBarItemMgr::RemoveItem, RemoveItem, RemoveItem method [Text Services Framework], RemoveItem method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_removeitem_ref, ctfutb/ITfLangBarItemMgr::RemoveItem, tsf.itflangbaritemmgr_removeitem
ms.topic: method
f1_keywords: 
 - "ctfutb/ITfLangBarItemMgr.RemoveItem"
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
 - ITfLangBarItemMgr.RemoveItem
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarItemMgr::RemoveItem


## -description




## -parameters




### -param punk [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object to remove from the language bar. The language bar will call <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a> and use the item <b>GUID</b> to identify the item to remove.


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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>
 

 

