---
UID: NF:ctfutb.ITfLangBarItemMgr.AdviseItemSink
title: ITfLangBarItemMgr::AdviseItemSink
author: windows-sdk-content
description: ITfLangBarItemMgr::AdviseItemSink method
old-location: tsf\itflangbaritemmgr_adviseitemsink.htm
old-project: TSF
ms.assetid: c01d80eb-9156-4fbf-98ff-7f06b145e72f
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: AdviseItemSink, AdviseItemSink method [Text Services Framework], AdviseItemSink method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AdviseItemSink method, ITfLangBarItemMgr.AdviseItemSink, ITfLangBarItemMgr::AdviseItemSink, _tsf_itflangbaritemmgr_adviseitemsink_ref, ctfutb/ITfLangBarItemMgr::AdviseItemSink, tsf.itflangbaritemmgr_adviseitemsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITfLangBarItemMgr.AdviseItemSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemMgr::AdviseItemSink


## -description




## -parameters




### -param punk [in]

Pointer to the <a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink</a> object to install.


### -param pdwCookie [out]

Pointer to a <b>DWORD</b> that receives an advise sink identification cookie. This cookie identifies the advise sink when it is removed with the <a href="https://msdn.microsoft.com/20a0f69b-950e-4ad7-9357-74f0b4a75c6b">ITfLangBarItemMgr::UnadviseItemSink</a> or <a href="https://msdn.microsoft.com/e15fb870-bedc-412d-9561-4db6c0515799">ITfLangBarItemMgr::UnadviseItemsSink</a> method.


### -param rguidItem [in]

Contains the <b>GUID</b> that identifies the item to install the advise sink for. This is the item <b>GUID</b> that the item supplies in <a href="https://msdn.microsoft.com/b32e433a-c0d6-418e-bf11-2291c85373c2">ITfLangBarItem::GetInfo</a>. This can be a custom value or one of the <a href="https://msdn.microsoft.com/6280cde9-2350-48a9-8740-01a856b0a1bc">predefined language bar items</a>.


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
<i>rguidItem</i> is invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>punk</i> and/or <i>pdwCookie</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b32e433a-c0d6-418e-bf11-2291c85373c2">ITfLangBarItem::GetInfo</a>



<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/20a0f69b-950e-4ad7-9357-74f0b4a75c6b">ITfLangBarItemMgr::UnadviseItemSink
      </a>



<a href="https://msdn.microsoft.com/e15fb870-bedc-412d-9561-4db6c0515799">
        ITfLangBarItemMgr::UnadviseItemsSink
      </a>



<a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink</a>



<a href="https://msdn.microsoft.com/6280cde9-2350-48a9-8740-01a856b0a1bc">
        Predefined language bar items
      </a>
 

 

