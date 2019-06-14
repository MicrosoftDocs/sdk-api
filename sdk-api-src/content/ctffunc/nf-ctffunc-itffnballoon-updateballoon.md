---
UID: NF:ctffunc.ITfFnBalloon.UpdateBalloon
title: ITfFnBalloon::UpdateBalloon (ctffunc.h)
author: windows-sdk-content
description: ITfFnBalloon::UpdateBalloon method
old-location: tsf\itffnballoon_updateballoon.htm
tech.root: TSF
ms.assetid: b395d587-02a7-496e-8bfd-8fcaba2a3edc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnBalloon interface [Text Services Framework],UpdateBalloon method, ITfFnBalloon.UpdateBalloon, ITfFnBalloon::UpdateBalloon, UpdateBalloon, UpdateBalloon method [Text Services Framework], UpdateBalloon method [Text Services Framework],ITfFnBalloon interface, _tsf_itffnballoon_updateballoon_ref, ctffunc/ITfFnBalloon::UpdateBalloon, tsf.itffnballoon_updateballoon
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnBalloon.UpdateBalloon
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnBalloon::UpdateBalloon


## -description




## -parameters




### -param style [in]

Contains one of the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/ne-ctfutb-__midl_itflangbaritemballoon_0001">TfLBBalloonStyle</a> values that specifies the new balloon style.


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



The language bar balloon implementation should update its style and text by modifying the values returned from <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getstatus">ITfLangBarItemBalloon::GetBalloonInfo</a> and then call <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_BALLOON to cause the language bar to obtain the updated information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itffnballoon">ITfFnBalloon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getstatus">ITfLangBarItemBalloon::GetBalloonInfo
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/ne-ctfutb-__midl_itflangbaritemballoon_0001">TfLBBalloonStyle
      </a>
 

 

