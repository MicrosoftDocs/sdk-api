---
UID: NN:ctfutb.ITfSystemLangBarItem
title: ITfSystemLangBarItem
author: windows-sdk-content
description: The ITfSystemLangBarItem interface is implemented by a system language bar menu and is used by a system language bar extension to modify the icon and/or tooltip string displayed for the menu.
old-location: tsf\itfsystemlangbaritem.htm
tech.root: TSF
ms.assetid: 9b41e787-eb90-4858-8838-8c36c7dce0c1
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfSystemLangBarItem, ITfSystemLangBarItem interface [Text Services Framework], ITfSystemLangBarItem interface [Text Services Framework],described, _tsf_itfsystemlangbaritem_ref, ctfutb/ITfSystemLangBarItem, tsf.itfsystemlangbaritem
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
 - ITfSystemLangBarItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfSystemLangBarItem interface


## -description


The <b>ITfSystemLangBarItem</b> interface is implemented by a system language bar menu and is used by a system language bar extension to modify the icon and/or tooltip string displayed for the menu. The extension can obtain an instance of this interface by by calling QueryInterface on the <a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a> object with IID_ITfSystemLangBarItem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemLangBarItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfSystemLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSystemLangBarItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b83e2ec-ac2f-4fd6-8c7c-70b00baafdc1">SetIcon</a>
</td>
<td align="left" width="63%">
Modifies the icon displayed for the system language bar menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6917fcd1-acce-4e5d-b04f-ee8ea69e71b4">SetTooltipString</a>
</td>
<td align="left" width="63%">
Modifies the tooltip text displayed for the system language bar menu.

</td>
</tr>
</table> 


## -remarks



A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> implementation. The system item should also implement the <b>ITfSystemLangBarItem</b> interface. The system item uses the <a href="https://msdn.microsoft.com/a88b20ec-fc54-4814-9ca1-131664b4f377">ITfSystemLangBarItemSink</a> interface to enable the extension to add items.




## -see-also




<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a>



<a href="https://msdn.microsoft.com/a88b20ec-fc54-4814-9ca1-131664b4f377">ITfSystemLangBarItemSink</a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

