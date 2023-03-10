---
UID: NF:ctfutb.ITfSystemLangBarItemSink.InitMenu
title: ITfSystemLangBarItemSink::InitMenu (ctfutb.h)
description: ITfSystemLangBarItemSink::InitMenu method
helpviewer_keywords: ["ITfSystemLangBarItemSink interface [Text Services Framework]","InitMenu method","ITfSystemLangBarItemSink.InitMenu","ITfSystemLangBarItemSink::InitMenu","InitMenu","InitMenu method [Text Services Framework]","InitMenu method [Text Services Framework]","ITfSystemLangBarItemSink interface","_tsf_itfsystemlangbaritemsink_initmenu_ref","ctfutb/ITfSystemLangBarItemSink::InitMenu","tsf.itfsystemlangbaritemsink_initmenu"]
old-location: tsf\itfsystemlangbaritemsink_initmenu.htm
tech.root: TSF
ms.assetid: 6e8ba0ef-2f0a-4d67-95c1-06fee763bc14
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItemSink interface [Text Services Framework],InitMenu method, ITfSystemLangBarItemSink.InitMenu, ITfSystemLangBarItemSink::InitMenu, InitMenu, InitMenu method [Text Services Framework], InitMenu method [Text Services Framework],ITfSystemLangBarItemSink interface, _tsf_itfsystemlangbaritemsink_initmenu_ref, ctfutb/ITfSystemLangBarItemSink::InitMenu, tsf.itfsystemlangbaritemsink_initmenu
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
 - ITfSystemLangBarItemSink::InitMenu
 - ctfutb/ITfSystemLangBarItemSink::InitMenu
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
 - ITfSystemLangBarItemSink.InitMenu
---

# ITfSystemLangBarItemSink::InitMenu


## -description

Called to allow a system language bar item extension to add items to a system language bar menu.

## -parameters

### -param pMenu [in]

Pointer to an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu</a> interface that the system language bar item uses to add items to the system language bar menu.

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
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink">ITfSystemLangBarItemSink</a>