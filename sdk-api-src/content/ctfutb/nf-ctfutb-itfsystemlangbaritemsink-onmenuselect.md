---
UID: NF:ctfutb.ITfSystemLangBarItemSink.OnMenuSelect
title: ITfSystemLangBarItemSink::OnMenuSelect
author: windows-sdk-content
description: ITfSystemLangBarItemSink::OnMenuSelect method
old-location: tsf\itfsystemlangbaritemsink_onmenuselect.htm
old-project: TSF
ms.assetid: 43c20f95-64b5-458a-8469-0d8b284b66dd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfSystemLangBarItemSink interface [Text Services Framework],OnMenuSelect method, ITfSystemLangBarItemSink.OnMenuSelect, ITfSystemLangBarItemSink::OnMenuSelect, OnMenuSelect, OnMenuSelect method [Text Services Framework], OnMenuSelect method [Text Services Framework],ITfSystemLangBarItemSink interface, _tsf_itfsystemlangbaritemsink_onmenuselect_ref, ctfutb/ITfSystemLangBarItemSink::OnMenuSelect, tsf.itfsystemlangbaritemsink_onmenuselect
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
 - Msctf.dll
api_name:
 - ITfSystemLangBarItemSink.OnMenuSelect
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemLangBarItemSink::OnMenuSelect


## -description




## -parameters




### -param wID [in]

Specifies the identifier of the menu item selected. This is the value passed for <i>uId</i> in <a href="https://msdn.microsoft.com/c00048d1-d7c1-4ea3-a132-5f5aa570148f">ITfMenu::AddMenuItem</a>.


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




<a href="https://msdn.microsoft.com/c00048d1-d7c1-4ea3-a132-5f5aa570148f">ITfMenu::AddMenuItem
      </a>



<a href="https://msdn.microsoft.com/a88b20ec-fc54-4814-9ca1-131664b4f377">ITfSystemLangBarItemSink</a>
 

 

