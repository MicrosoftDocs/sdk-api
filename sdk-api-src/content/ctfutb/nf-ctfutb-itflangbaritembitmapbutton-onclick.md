---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.OnClick
title: ITfLangBarItemBitmapButton::OnClick
author: windows-sdk-content
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.
old-location: tsf\itflangbaritembitmapbutton_onclick.htm
old-project: TSF
ms.assetid: 8d376d22-897d-4032-9c9e-7d0f93d73fac
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfLangBarItemBitmapButton interface [Text Services Framework],OnClick method, ITfLangBarItemBitmapButton.OnClick, ITfLangBarItemBitmapButton::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemBitmapButton interface, _tsf_itflangbaritembitmapbutton_onclick_ref, ctfutb/ITfLangBarItemBitmapButton::OnClick, tsf.itflangbaritembitmapbutton_onclick
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemBitmapButton.OnClick
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemBitmapButton::OnClick


## -description


This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.


## -parameters




### -param click [in]

Contains a <a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick</a> value that indicates which mouse button was used to click the button.


### -param pt [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the position, in screen coordinates, of the mouse cursor at the time of the click event.


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




<a href="https://msdn.microsoft.com/29fcc913-fcc7-4321-918b-2c354dd751ff">ITfLangBarItemBitmapButton</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick
      </a>
 

 

