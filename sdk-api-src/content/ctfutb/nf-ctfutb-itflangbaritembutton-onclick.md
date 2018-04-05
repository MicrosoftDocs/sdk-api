---
UID: NF:ctfutb.ITfLangBarItemButton.OnClick
title: ITfLangBarItemButton::OnClick method
author: windows-driver-content
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.
old-location: tsf\itflangbaritembutton_onclick.htm
old-project: TSF
ms.assetid: c725ee0b-57fe-4860-aa49-af61f2c7fa32
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfLangBarItemButton, ITfLangBarItemButton interface [Text Services Framework], OnClick method, ITfLangBarItemButton::OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework], ITfLangBarItemButton interface, OnClick,ITfLangBarItemButton.OnClick, _tsf_itflangbaritembutton_onclick_ref, ctfutb/ITfLangBarItemButton::OnClick, tsf.itflangbaritembutton_onclick
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
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfLangBarItemButton.OnClick
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemButton::OnClick method


## -description


This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.


## -parameters




### -param click [in]

Contains one of the <a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick</a> values that indicate which mouse button was used to click the button.


### -param pt [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the position of the mouse cursor, in screen coordinates, at the time of the click event.


### -param prcArea [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the bounding rectangle, in screen coordinates, of the button.


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
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/098a8cdc-ff34-4729-9b34-279c499d40a8">ITfLangBarItemButton</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick
      </a>
 

 

