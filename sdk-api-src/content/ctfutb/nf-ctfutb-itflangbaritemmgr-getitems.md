---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItems
title: ITfLangBarItemMgr::GetItems (ctfutb.h)
description: ITfLangBarItemMgr::GetItems method
helpviewer_keywords: ["GetItems","GetItems method [Text Services Framework]","GetItems method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","GetItems method","ITfLangBarItemMgr.GetItems","ITfLangBarItemMgr::GetItems","_tsf_itflangbaritemmgr_getitems_ref","ctfutb/ITfLangBarItemMgr::GetItems","tsf.itflangbaritemmgr_getitems"]
old-location: tsf\itflangbaritemmgr_getitems.htm
tech.root: TSF
ms.assetid: b6342d4b-e2b6-47d7-9f66-b3aa329c480d
ms.date: 12/05/2018
ms.keywords: GetItems, GetItems method [Text Services Framework], GetItems method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItems method, ITfLangBarItemMgr.GetItems, ITfLangBarItemMgr::GetItems, _tsf_itflangbaritemmgr_getitems_ref, ctfutb/ITfLangBarItemMgr::GetItems, tsf.itflangbaritemmgr_getitems
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
 - ITfLangBarItemMgr::GetItems
 - ctfutb/ITfLangBarItemMgr::GetItems
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
 - ITfLangBarItemMgr.GetItems
---

# ITfLangBarItemMgr::GetItems


## -description

Obtains the interface, information and status for one or more items in the language bar.

## -parameters

### -param ulCount [in]

Specifies the number of items to obtain the status for.

### -param ppItem [out]

Pointer to an array of <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> interface pointers that receive the item interfaces. This array must be at least <i>ulCount</i> elements in length.

### -param pInfo

[in, out] Pointer to an array of <a href="/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo">TF_LANGBARITEMINFO</a> structures that receive the information for each item. This array must be at least <i>ulCount</i> elements in length.

### -param pdwStatus

[in, out] Pointer to an array of <b>DWORD</b> values that receive the status of each item. Each element in this array receives zero or a combination of one or more of the <a href="/windows/desktop/TSF/tf-lbi-status--constants">TF_LBI_STATUS_*</a> values. This array must be at least <i>ulCount</i> elements in length.

### -param pcFetched

[in, out] Pointer to a ULONG that receives the number of items obtained by this method. This parameter can be <b>NULL</b> if this information is not required.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of items obtained is less than the number of items requested. If <i>pcFetched</i> is not <b>NULL</b>, <i>pcFetched</i> receives the number of items obtained.

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
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo">TF_LANGBARITEMINFO</a>



<a href="/windows/desktop/TSF/tf-lbi-status--constants">TF_LBI_STATUS_* Constants
      </a>