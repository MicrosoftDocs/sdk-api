---
UID: NF:ctfutb.ITfLangBarItem.GetStatus
title: ITfLangBarItem::GetStatus (ctfutb.h)
description: ITfLangBarItem::GetStatus method
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITfLangBarItem interface","ITfLangBarItem interface [Text Services Framework]","GetStatus method","ITfLangBarItem.GetStatus","ITfLangBarItem::GetStatus","_tsf_itflangbaritem_getstatus_ref","ctfutb/ITfLangBarItem::GetStatus","tsf.itflangbaritem_getstatus"]
old-location: tsf\itflangbaritem_getstatus.htm
tech.root: TSF
ms.assetid: 2f850553-ec79-4e2f-a4d5-c40dbaca0f01
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfLangBarItem interface, ITfLangBarItem interface [Text Services Framework],GetStatus method, ITfLangBarItem.GetStatus, ITfLangBarItem::GetStatus, _tsf_itflangbaritem_getstatus_ref, ctfutb/ITfLangBarItem::GetStatus, tsf.itflangbaritem_getstatus
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
 - ITfLangBarItem::GetStatus
 - ctfutb/ITfLangBarItem::GetStatus
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
 - ITfLangBarItem.GetStatus
---

# ITfLangBarItem::GetStatus


## -description

Obtains the status of a language bar item.

## -parameters

### -param pdwStatus [out]

Pointer to a <b>DWORD</b> that receives zero or a combination of one or more of the <a href="/windows/desktop/TSF/tf-lbi-status--constants">TF_LBI_STATUS_*</a> values that indicate the current status of the item.

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
<i>pdwStatus</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/TSF/tf-lbi-status--constants">TF_LBI_STATUS_*
      </a>