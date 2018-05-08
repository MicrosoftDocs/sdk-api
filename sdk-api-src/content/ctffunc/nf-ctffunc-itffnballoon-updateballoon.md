---
UID: NF:ctffunc.ITfFnBalloon.UpdateBalloon
title: ITfFnBalloon::UpdateBalloon
author: windows-driver-content
description: ITfFnBalloon::UpdateBalloon method
old-location: tsf\itffnballoon_updateballoon.htm
old-project: TSF
ms.assetid: b395d587-02a7-496e-8bfd-8fcaba2a3edc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfFnBalloon interface [Text Services Framework],UpdateBalloon method, ITfFnBalloon.UpdateBalloon, ITfFnBalloon::UpdateBalloon, UpdateBalloon, UpdateBalloon method [Text Services Framework], UpdateBalloon method [Text Services Framework],ITfFnBalloon interface, _tsf_itffnballoon_updateballoon_ref, ctffunc/ITfFnBalloon::UpdateBalloon, tsf.itffnballoon_updateballoon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFnBalloon.UpdateBalloon
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnBalloon::UpdateBalloon


## -description




## -parameters




### -param style [in]

Contains one of the <a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle</a> values that specifies the new balloon style.


### -param pch [in]

Pointer to a <b>WCHAR</b> buffer that contains the new text for the balloon.


### -param cch [in]

Contains the number of characters of the new text in <i>pch</i>.


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
 




## -remarks



The language bar balloon implementation should update its style and text by modifying the values returned from <a href="https://msdn.microsoft.com/2f850553-ec79-4e2f-a4d5-c40dbaca0f01">ITfLangBarItemBalloon::GetBalloonInfo</a> and then call <a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_BALLOON to cause the language bar to obtain the updated information.




## -see-also




<a href="https://msdn.microsoft.com/9b79526b-b7e1-41a2-b32e-88124347d77d">ITfFnBalloon</a>



<a href="https://msdn.microsoft.com/2f850553-ec79-4e2f-a4d5-c40dbaca0f01">
        ITfLangBarItemBalloon::GetBalloonInfo
      </a>



<a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">
        ITfLangBarItemSink::OnUpdate
      </a>



<a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle
      </a>
 

 

