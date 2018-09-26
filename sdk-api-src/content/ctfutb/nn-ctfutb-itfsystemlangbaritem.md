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


The <b>ITfSystemLangBarItem</b> interface is implemented by a system language bar menu and is used by a system language bar extension to modify the icon and/or tooltip string displayed for the menu. The extension can obtain an instance of this interface by by calling QueryInterface on the <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> object with IID_ITfSystemLangBarItem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemLangBarItem</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfSystemLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms628960(v=VS.85).aspx">SetIcon</a>
</td>
<td align="left" width="63%">
Modifies the icon displayed for the system language bar menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628961(v=VS.85).aspx">SetTooltipString</a>
</td>
<td align="left" width="63%">
Modifies the tooltip text displayed for the system language bar menu.

</td>
</tr>
</table> 


## -remarks



A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="https://msdn.microsoft.com/en-us/library/ms628941(v=VS.85).aspx">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <a href="https://msdn.microsoft.com/en-us/library/ms628945(v=VS.85).aspx">ITfSource::AdviseSink</a> implementation. The system item should also implement the <b>ITfSystemLangBarItem</b> interface. The system item uses the <a href="https://msdn.microsoft.com/en-us/library/ms628957(v=VS.85).aspx">ITfSystemLangBarItemSink</a> interface to enable the extension to add items.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms628941(v=VS.85).aspx">ITfSource</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628945(v=VS.85).aspx">ITfSource::AdviseSink</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628957(v=VS.85).aspx">ITfSystemLangBarItemSink</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

