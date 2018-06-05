---
UID: NF:ctfutb.ITfLangBarItemButton.GetIcon
title: ITfLangBarItemButton::GetIcon
author: windows-sdk-content
description: ITfLangBarItemButton::GetIcon method
old-location: tsf\itflangbaritembutton_geticon.htm
old-project: TSF
ms.assetid: 6134f747-a138-4ec4-8a89-c25beddcf319
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetIcon, GetIcon method [Text Services Framework], GetIcon method [Text Services Framework],ITfLangBarItemButton interface, ITfLangBarItemButton interface [Text Services Framework],GetIcon method, ITfLangBarItemButton.GetIcon, ITfLangBarItemButton::GetIcon, _tsf_itflangbaritembutton_geticon_ref, ctfutb/ITfLangBarItemButton::GetIcon, tsf.itflangbaritembutton_geticon
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
tech.root: 
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfLangBarItemButton.GetIcon
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemButton::GetIcon


## -description




## -parameters




### -param phIcon [out]

Pointer to an <b>HICON</b> value that receives the icon handle. Receives <b>NULL</b> if the button has no icon. The caller must free this icon when it is no longer required by calling <b>DestroyIcon</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>phIcon</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



The ideal size of the icon can be obtained by calling GetSystemMetrics(SM_CXSMICON) for the icon width and GetSystemMetrics(SM_CYSMICON) for the icon height.

If the button has the TF_LBI_STYLE_TEXTCOLORICON style, the icon obtained by this method should be a monochrome icon.



