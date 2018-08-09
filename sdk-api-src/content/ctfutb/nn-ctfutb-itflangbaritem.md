---
UID: NN:ctfutb.ITfLangBarItem
title: ITfLangBarItem
author: windows-sdk-content
description: The ITfLangBarItem interface is implemented by a language bar item provider and used by the language bar manager to obtain detailed information about the language bar item.
old-location: tsf\itflangbaritem.htm
old-project: TSF
ms.assetid: 16612641-2bff-4e6f-a955-85793021a20b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfLangBarItem, ITfLangBarItem interface [Text Services Framework], ITfLangBarItem interface [Text Services Framework],described, _tsf_itflangbaritem_ref, ctfutb/ITfLangBarItem, tsf.itflangbaritem
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
 - ITfLangBarItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItem interface


## -description


The <b>ITfLangBarItem</b> interface is implemented by a language bar item provider and used by the language bar manager to obtain detailed information about the language bar item. An instance of this interface is provided to the language bar manager by the <a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">ITfLangBarItemMgr::AddItem</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Obtains information about the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0bb3c7f-c21e-443a-965a-0601de0210b5">GetTooltipString</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed in the tooltip for the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f5be2f4-e9de-4b03-9c37-651b1e572cf0">Show</a>
</td>
<td align="left" width="63%">
Called to show or hide the language bar item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">ITfLangBarItemMgr::AddItem
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

