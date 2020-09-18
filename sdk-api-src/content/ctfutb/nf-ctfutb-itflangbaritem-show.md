---
UID: NF:ctfutb.ITfLangBarItem.Show
title: ITfLangBarItem::Show (ctfutb.h)
description: ITfLangBarItem::Show method
helpviewer_keywords: ["ITfLangBarItem interface [Text Services Framework]","Show method","ITfLangBarItem.Show","ITfLangBarItem::Show","Show","Show method [Text Services Framework]","Show method [Text Services Framework]","ITfLangBarItem interface","_tsf_itflangbaritem_show_ref","ctfutb/ITfLangBarItem::Show","tsf.itflangbaritem_show"]
old-location: tsf\itflangbaritem_show.htm
tech.root: TSF
ms.assetid: 3f5be2f4-e9de-4b03-9c37-651b1e572cf0
ms.date: 12/05/2018
ms.keywords: ITfLangBarItem interface [Text Services Framework],Show method, ITfLangBarItem.Show, ITfLangBarItem::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfLangBarItem interface, _tsf_itflangbaritem_show_ref, ctfutb/ITfLangBarItem::Show, tsf.itflangbaritem_show
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
 - ITfLangBarItem::Show
 - ctfutb/ITfLangBarItem::Show
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
 - ITfLangBarItem.Show
---

# ITfLangBarItem::Show


## -description

Called to show or hide the language bar item.

## -parameters

### -param fShow [in]

Contains a <b>BOOL</b> that indicates if the item should be shown or hidden. Contains a nonzero value if the item should be shown or zero otherwise.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The language bar item does not support this method.

</td>
</tr>
</table>

## -remarks

The language bar item implementation should update its visible status by modifying the value returned from <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getstatus">ITfLangBarItem::GetStatus</a> to include or exclude the TF_LBI_STATUS_HIDDEN status flag. The implementation then prompts language bar to obtain the new status value by calling <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_STATUS.

This method is only useful when the item has the TF_LBI_STYLE_HIDDENSTATUSCONTROL style. Without this style, only the language bar can show or hide the item.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getstatus">ITfLangBarItem::GetStatus
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate
      </a>