---
UID: NN:ctfutb.ITfLangBarItemBalloon
title: ITfLangBarItemBalloon
author: windows-sdk-content
description: The ITfLangBarItemBalloon interface is implemented by an application or text service and is used by the language bar manager to obtain information specific to a balloon item on the language bar.
old-location: tsf\itflangbaritemballoon.htm
tech.root: TSF
ms.assetid: 619a6f21-fbac-455c-a702-0302ce13112b
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfLangBarItemBalloon, ITfLangBarItemBalloon interface [Text Services Framework], ITfLangBarItemBalloon interface [Text Services Framework],described, _tsf_itflangbaritemballoon_ref, ctfutb/ITfLangBarItemBalloon, tsf.itflangbaritemballoon
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
 - ITfLangBarItemBalloon
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBalloon interface


## -description


The <b>ITfLangBarItemBalloon</b> interface is implemented by an application or text service and is used by the language bar manager to obtain information specific to a balloon item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> passed to <a href="https://msdn.microsoft.com/en-us/library/ms628724(v=VS.85).aspx">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBalloon.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemBalloon</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfLangBarItemBalloon</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemBalloon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628703(v=VS.85).aspx">GetBalloonInfo</a>
</td>
<td align="left" width="63%">
Obtains information about the balloon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628704(v=VS.85).aspx">GetPreferredSize</a>
</td>
<td align="left" width="63%">
Obtains the preferred size,in pixels, of the balloon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628705(v=VS.85).aspx">OnClick</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
</table> 


## -remarks



A language bar balloon acts as a pop-up notification on the language bar.




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem
      </a>



<a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">ITfLangBarItemMgr::AddItem
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

