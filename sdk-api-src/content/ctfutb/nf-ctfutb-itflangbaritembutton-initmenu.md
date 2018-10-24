---
UID: NF:ctfutb.ITfLangBarItemButton.InitMenu
title: ITfLangBarItemButton::InitMenu
author: windows-sdk-content
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.
old-location: tsf\itflangbaritembutton_initmenu.htm
tech.root: TSF
ms.assetid: 6f9debf8-1c25-4228-abd2-2b2a099cf5cd
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfLangBarItemButton interface [Text Services Framework],InitMenu method, ITfLangBarItemButton.InitMenu, ITfLangBarItemButton::InitMenu, InitMenu, InitMenu method [Text Services Framework], InitMenu method [Text Services Framework],ITfLangBarItemButton interface, _tsf_itflangbaritembutton_initmenu_ref, ctfutb/ITfLangBarItemButton::InitMenu, tsf.itflangbaritembutton_initmenu
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
 - ITfLangBarItemButton.InitMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemButton::InitMenu


## -description


This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.


## -parameters




### -param pMenu [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628780(v=VS.85).aspx">ITfMenu</a> interface that the language bar button uses to add items to the menu that the language bar displays for the button.


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




<a href="https://msdn.microsoft.com/en-us/library/ms628717(v=VS.85).aspx">ITfLangBarItemButton</a>



<a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu
      </a>
 

 

