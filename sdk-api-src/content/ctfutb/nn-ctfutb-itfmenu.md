---
UID: NN:ctfutb.ITfMenu
title: ITfMenu
author: windows-sdk-content
description: The ITfMenu interface is implemented by the language bar and used by a language bar button provider to add items to the menu that the language bar will display for the button.
old-location: tsf\itfmenu.htm
tech.root: TSF
ms.assetid: 303115e1-8d52-4a0a-b05e-b5c92b8b3e2a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfMenu, ITfMenu interface [Text Services Framework], ITfMenu interface [Text Services Framework],described, _tsf_itfmenu_ref, ctfutb/ITfMenu, tsf.itfmenu
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfMenu interface


## -description


The <b>ITfMenu</b> interface is implemented by the language bar and used by a language bar button provider to add items to the menu that the language bar will display for the button.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMenu</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c00048d1-d7c1-4ea3-a132-5f5aa570148f">AddMenuItem</a>
</td>
<td align="left" width="63%">
Adds an item to the menu that the language bar will display for the button.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f34f488-729b-42d3-9a24-85b3f95607ec">ITfLangBarItemBitmapButton::InitMenu
      </a>



<a href="https://msdn.microsoft.com/6f9debf8-1c25-4228-abd2-2b2a099cf5cd">ITfLangBarItemButton::InitMenu
      </a>



<a href="https://msdn.microsoft.com/6e8ba0ef-2f0a-4d67-95c1-06fee763bc14">ITfSystemLangBarItemSink::InitMenu
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

