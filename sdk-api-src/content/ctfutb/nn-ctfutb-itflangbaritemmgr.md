---
UID: NN:ctfutb.ITfLangBarItemMgr
title: ITfLangBarItemMgr (ctfutb.h)
description: The ITfLangBarItemMgr interface is implemented by the language bar and used by a text service to manage items in the language bar.
old-location: tsf\itflangbaritemmgr.htm
tech.root: TSF
ms.assetid: a7fa257f-e600-4554-8b23-f73323f37e69
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr, ITfLangBarItemMgr interface [Text Services Framework], ITfLangBarItemMgr interface [Text Services Framework],described, _tsf_itflangbaritemmgr_ref, ctfutb/ITfLangBarItemMgr, tsf.itflangbaritemmgr
f1_keywords:
- ctfutb/ITfLangBarItemMgr
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
- ITfLangBarItemMgr
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarItemMgr interface


## -description


The <b>ITfLangBarItemMgr</b> interface is implemented by the language bar and used by a text service to manage items in the language bar.

A text service obtains an instance of this interface by calling ITfThreadMgr::QueryInterface with IID_ITfLangBarItemMgr. An instance of this interface can also be created by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_LangBarItemMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">AddItem</a>
</td>
<td align="left" width="63%">
Adds an item to the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">AdviseItemSink</a>
</td>
<td align="left" width="63%">
Installs a language bar item event sink for a language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">AdviseItemsSink</a>
</td>
<td align="left" width="63%">
Installs one or more language bar item event sinks for one or more language bar items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-enumitems">EnumItems</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Obtains the ITfLangBarItem interface for an item in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitemfloatingrect">GetItemFloatingRect</a>
</td>
<td align="left" width="63%">
Obtains the bounding rectangle of an item on the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitemnum">GetItemNum</a>
</td>
<td align="left" width="63%">
Obtains the number of items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitems">GetItems</a>
</td>
<td align="left" width="63%">
Obtains the interface, information and status for one or more items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitemsstatus">GetItemsStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of one or more items on the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes an item from the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemsink">UnadviseItemSink</a>
</td>
<td align="left" width="63%">
Removes a language bar item event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemssink">UnadviseItemsSink</a>
</td>
<td align="left" width="63%">
Removes one or more language bar item event sinks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

