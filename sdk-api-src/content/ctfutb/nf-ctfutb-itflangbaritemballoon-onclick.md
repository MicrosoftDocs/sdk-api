---
UID: NF:ctfutb.ITfLangBarItemBalloon.OnClick
title: ITfLangBarItemBalloon::OnClick
author: windows-sdk-content
description: ITfLangBarItemBalloon::OnClick method
old-location: tsf\itflangbaritemballoon_onclick.htm
tech.root: TSF
ms.assetid: 52592a39-8b79-4e9c-9d8b-1100c9f36eca
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITfLangBarItemBalloon interface [Text Services Framework],OnClick method, ITfLangBarItemBalloon.OnClick, ITfLangBarItemBalloon::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemBalloon interface, _tsf_itflangbaritemballoon_onclick_ref, ctfutb/ITfLangBarItemBalloon::OnClick, tsf.itflangbaritemballoon_onclick
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
 - ITfLangBarItemBalloon.OnClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- ctfutb.h
: 
- ITfLangBarItemBalloon.OnClick
: 
---

# ITfLangBarItemBalloon::OnClick


## -description




## -parameters




### -param click [in]

Contains one of the <a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick</a> values that indicate which mouse button was used to click the balloon.


### -param pt [in]

Pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the position of the mouse cursor, in screen coordinates, at the time of the click event.


### -param prcArea [in]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the bounding rectangle, in screen coordinates, of the balloon.


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




<a href="https://msdn.microsoft.com/619a6f21-fbac-455c-a702-0302ce13112b">ITfLangBarItemBalloon</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/7fd151dd-e4be-4ec8-b373-2115717d5ef4">TfLBIClick
      </a>
 

 

