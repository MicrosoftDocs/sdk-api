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
req.redist: TSF 1.0 on Windows 2000 Professional
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


The <b>ITfLangBarItem</b> interface is implemented by a language bar item provider and used by the language bar manager to obtain detailed information about the language bar item. An instance of this interface is provided to the language bar manager by the <a href="https://msdn.microsoft.com/en-us/library/ms628724(v=VS.85).aspx">ITfLangBarItemMgr::AddItem</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItem</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms628741(v=VS.85).aspx">GetInfo</a>
</td>
<td align="left" width="63%">
Obtains information about the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628743(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628744(v=VS.85).aspx">GetTooltipString</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed in the tooltip for the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628746(v=VS.85).aspx">Show</a>
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
 

 

