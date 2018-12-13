---
UID: NN:ctfutb.ITfLangBarItemBitmapButton
title: ITfLangBarItemBitmapButton
author: windows-sdk-content
description: The ITfLangBarItemBitmapButton interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.
old-location: tsf\itflangbaritembitmapbutton.htm
tech.root: TSF
ms.assetid: 29fcc913-fcc7-4321-918b-2c354dd751ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfLangBarItemBitmapButton, ITfLangBarItemBitmapButton interface [Text Services Framework], ITfLangBarItemBitmapButton interface [Text Services Framework],described, _tsf_itflangbaritembitmapbutton_ref, ctfutb/ITfLangBarItemBitmapButton, tsf.itflangbaritembitmapbutton
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
 - ITfLangBarItemBitmapButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmapButton interface


## -description


The <b>ITfLangBarItemBitmapButton</b> interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a> passed to <a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBitmapButton.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemBitmapButton</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarItemBitmapButton</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemBitmapButton</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/412b2e74-0569-4f72-bc8e-23edec72ea35">DrawBitmap</a>
</td>
<td align="left" width="63%">
Obtains the bitmap and mask for the bitmap button item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/271e4e24-c81e-484c-84bb-d7b67038a5c5">GetPreferredSize</a>
</td>
<td align="left" width="63%">
Obtains the preferred size, in pixels, of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac37ea79-59bb-44c1-aace-b3c0dccfd377">GetText</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed for the bitmap button in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f34f488-729b-42d3-9a24-85b3f95607ec">InitMenu</a>
</td>
<td align="left" width="63%">
Called to enable a language bar bitmap button, that has the TF_LBI_STYLE_BTN_MENU style, to add items to the menu that the language bar will display for the button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d376d22-897d-4032-9c9e-7d0f93d73fac">OnClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks a language bar bitmap button that has the TF_LBI_STYLE_BTN_BUTTON or TF_LBI_STYLE_BTN_TOGGLE style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/693f68ce-e557-4c66-9a6d-ba76e4fde426">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the menu that the language bar displays for the button.

</td>
</tr>
</table> 


## -remarks



A language bar bitmap button functions as a button item on the language bar that displays text and a small bitmap. The bitmap displayed for the item should not be larger than the size of a small icon. Obtain these dimensions by calling <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> with SM_CXSMICON for the width and SM_CYSMICON for the height.




## -see-also




<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem
      </a>



<a href="https://msdn.microsoft.com/c9a36b2c-e7ea-4932-928e-05dd05ca02ca">ITfLangBarItemMgr::AddItem
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

