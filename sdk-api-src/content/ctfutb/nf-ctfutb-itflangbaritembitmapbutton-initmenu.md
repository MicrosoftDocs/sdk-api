---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.InitMenu
title: ITfLangBarItemBitmapButton::InitMenu
author: windows-sdk-content
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.
old-location: tsf\itflangbaritembitmapbutton_initmenu.htm
tech.root: TSF
ms.assetid: 0f34f488-729b-42d3-9a24-85b3f95607ec
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfLangBarItemBitmapButton interface [Text Services Framework],InitMenu method, ITfLangBarItemBitmapButton.InitMenu, ITfLangBarItemBitmapButton::InitMenu, InitMenu, InitMenu method [Text Services Framework], InitMenu method [Text Services Framework],ITfLangBarItemBitmapButton interface, _tsf_itflangbaritembitmapbutton_initmenu_ref, ctfutb/ITfLangBarItemBitmapButton::InitMenu, tsf.itflangbaritembitmapbutton_initmenu
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfLangBarItemBitmapButton.InitMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmapButton::InitMenu


## -description


This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.


## -parameters




### -param pMenu [in]

Pointer to an <a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu</a> interface that the language bar bitmap button uses to add items to the menu that the language bar displays for the button.


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




<a href="https://msdn.microsoft.com/29fcc913-fcc7-4321-918b-2c354dd751ff">ITfLangBarItemBitmapButton</a>



<a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu
      </a>
 

 

