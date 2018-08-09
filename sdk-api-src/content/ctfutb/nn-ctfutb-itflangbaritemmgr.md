---
UID: NN:ctfutb.ITfLangBarItemMgr
title: ITfLangBarItemMgr
author: windows-sdk-content
description: The ITfLangBarItemMgr interface is implemented by the language bar and used by a text service to manage items in the language bar.
old-location: tsf\itflangbaritemmgr.htm
old-project: TSF
ms.assetid: a7fa257f-e600-4554-8b23-f73323f37e69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfLangBarItemMgr, ITfLangBarItemMgr interface [Text Services Framework], ITfLangBarItemMgr interface [Text Services Framework],described, _tsf_itflangbaritemmgr_ref, ctfutb/ITfLangBarItemMgr, tsf.itflangbaritemmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TfLBIClick
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemMgr interface


## -description


The <b>ITfLangBarItemMgr</b> interface is implemented by the language bar and used by a text service to manage items in the language bar.

A text service obtains an instance of this interface by calling ITfThreadMgr::QueryInterface with IID_ITfLangBarItemMgr. An instance of this interface can also be created by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with CLSID_TF_LangBarItemMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarItemMgr</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">AddItem</a>
</td>
<td align="left" width="63%">
Adds an item to the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">AdviseItemSink</a>
</td>
<td align="left" width="63%">
Installs a language bar item event sink for a language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">AdviseItemsSink</a>
</td>
<td align="left" width="63%">
Installs one or more language bar item event sinks for one or more language bar items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90d61009-e0f7-4df6-a23b-1f9f489b15f9">EnumItems</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35895fd7-23d0-416b-98c2-45192edf0a6b">GetItem</a>
</td>
<td align="left" width="63%">
Obtains the ITfLangBarItem interface for an item in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56f30b8e-9e71-4b4e-a7df-e83d24cab297">GetItemFloatingRect</a>
</td>
<td align="left" width="63%">
Obtains the bounding rectangle of an item on the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0caf54b1-f862-4fc2-b593-c0e9f60d71cc">GetItemNum</a>
</td>
<td align="left" width="63%">
Obtains the number of items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6342d4b-e2b6-47d7-9f66-b3aa329c480d">GetItems</a>
</td>
<td align="left" width="63%">
Obtains the interface, information and status for one or more items in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf0bbbd5-63ca-4f2e-afee-e0c47d6e3d7b">GetItemsStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of one or more items on the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a56a8f4-8011-4847-869f-c859ec90da3b">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes an item from the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20a0f69b-950e-4ad7-9357-74f0b4a75c6b">UnadviseItemSink</a>
</td>
<td align="left" width="63%">
Removes a language bar item event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e15fb870-bedc-412d-9561-4db6c0515799">UnadviseItemsSink</a>
</td>
<td align="left" width="63%">
Removes one or more language bar item event sinks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

