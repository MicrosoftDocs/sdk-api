---
UID: NF:wmp.IWMPPlayer2.put_stretchToFit
title: IWMPPlayer2::put_stretchToFit (wmp.h)
description: The put_stretchToFit method specifies a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window when the video window is larger than the dimensions of the video image.helpviewer_keywords: ["IWMPPlayer2 interface [Windows Media Player]","put_stretchToFit method","IWMPPlayer2.put_stretchToFit","IWMPPlayer2::put_stretchToFit","IWMPPlayer2put_stretchToFit","put_stretchToFit","put_stretchToFit method [Windows Media Player]","put_stretchToFit method [Windows Media Player]","IWMPPlayer2 interface","wmp.iwmpplayer2_put_stretchtofit","wmp/IWMPPlayer2::put_stretchToFit"]
old-location: wmp\iwmpplayer2_put_stretchtofit.htm
tech.root: WMP
ms.assetid: 1da60976-5f84-4dc7-8186-32f6d3bb9165
ms.date: 12/05/2018
ms.keywords: IWMPPlayer2 interface [Windows Media Player],put_stretchToFit method, IWMPPlayer2.put_stretchToFit, IWMPPlayer2::put_stretchToFit, IWMPPlayer2put_stretchToFit, put_stretchToFit, put_stretchToFit method [Windows Media Player], put_stretchToFit method [Windows Media Player],IWMPPlayer2 interface, wmp.iwmpplayer2_put_stretchtofit, wmp/IWMPPlayer2::put_stretchToFit
f1_keywords:
- wmp/IWMPPlayer2.put_stretchToFit
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPPlayer2.put_stretchToFit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer2::put_stretchToFit


## -description



The <b>put_stretchToFit</b> method specifies a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window when the video window is larger than the dimensions of the video image.




## -parameters




### -param bEnabled [in]

<b>VARIANT_BOOL</b> indicating whether video displayed by the Windows Media Player control automatically resizes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



When the <b>VARIANT_BOOL</b> specified in <b>put_stretchToFit</b> is set to <b>TRUE</b>, the Windows Media Player control maintains the original aspect ratio of the video. If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and bottom or left and right of the video image.

This method applies to the Windows Media Player control only when embedded in a webpage.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-get_stretchtofit">IWMPPlayer2::get_stretchToFit</a>
 

 

