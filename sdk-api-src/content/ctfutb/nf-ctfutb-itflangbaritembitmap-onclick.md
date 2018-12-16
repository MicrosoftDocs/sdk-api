---
UID: NF:ctfutb.ITfLangBarItemBitmap.OnClick
title: ITfLangBarItemBitmap::OnClick
author: windows-sdk-content
description: ITfLangBarItemBitmap::OnClick method
old-location: tsf\itflangbaritembitmap_onclick.htm
tech.root: TSF
ms.assetid: b4e5857e-7e0b-462d-90cd-cb0e7b1143d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfLangBarItemBitmap interface [Text Services Framework],OnClick method, ITfLangBarItemBitmap.OnClick, ITfLangBarItemBitmap::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemBitmap interface, _tsf_itflangbaritembitmap_onclick_ref, ctfutb/ITfLangBarItemBitmap::OnClick, tsf.itflangbaritembitmap_onclick
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
 - ITfLangBarItemBitmap.OnClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmap::OnClick


## -description




## -parameters




### -param click [in]

Contains one of the <a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick</a> values that indicate which mouse button was used to click the bitmap.


### -param pt [in]

Pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the position of the mouse cursor, in screen coordinates, at the time of the click event.


### -param prcArea [in]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the bounding rectangle, in screen coordinates, of the bitmap.


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




<a href="https://msdn.microsoft.com/3bae0422-625e-4f7d-9845-5353ad3ff335">ITfLangBarItemBitmap</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick
      </a>
 

 

