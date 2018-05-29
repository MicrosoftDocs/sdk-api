---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.OnMenuSelect
title: ITfLangBarItemBitmapButton::OnMenuSelect
author: windows-sdk-content
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.
old-location: tsf\itflangbaritembitmapbutton_onmenuselect.htm
old-project: TSF
ms.assetid: 693f68ce-e557-4c66-9a6d-ba76e4fde426
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfLangBarItemBitmapButton interface [Text Services Framework],OnMenuSelect method, ITfLangBarItemBitmapButton.OnMenuSelect, ITfLangBarItemBitmapButton::OnMenuSelect, OnMenuSelect, OnMenuSelect method [Text Services Framework], OnMenuSelect method [Text Services Framework],ITfLangBarItemBitmapButton interface, _tsf_itflangbaritembitmapbutton_onmenuselect_ref, ctfutb/ITfLangBarItemBitmapButton::OnMenuSelect, tsf.itflangbaritembitmapbutton_onmenuselect
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
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfLangBarItemBitmapButton.OnMenuSelect
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemBitmapButton::OnMenuSelect


## -description


This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.


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




<a href="https://msdn.microsoft.com/29fcc913-fcc7-4321-918b-2c354dd751ff">ITfLangBarItemBitmapButton</a>



<a href="https://msdn.microsoft.com/c00048d1-d7c1-4ea3-a132-5f5aa570148f">ITfMenu::AddMenuItem
      </a>
 

 

