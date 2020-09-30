---
UID: NF:wmp.IWMPPlayer2.get_stretchToFit
title: IWMPPlayer2::get_stretchToFit (wmp.h)
description: The get_stretchToFit method retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window when the video window is larger than the dimensions of the video image.
helpviewer_keywords: ["IWMPPlayer2 interface [Windows Media Player]","get_stretchToFit method","IWMPPlayer2.get_stretchToFit","IWMPPlayer2::get_stretchToFit","IWMPPlayer2get_stretchToFit","get_stretchToFit","get_stretchToFit method [Windows Media Player]","get_stretchToFit method [Windows Media Player]","IWMPPlayer2 interface","wmp.iwmpplayer2_get_stretchtofit","wmp/IWMPPlayer2::get_stretchToFit"]
old-location: wmp\iwmpplayer2_get_stretchtofit.htm
tech.root: WMP
ms.assetid: d477800d-fb16-49a7-ab80-a0f5f7c68fc7
ms.date: 12/05/2018
ms.keywords: IWMPPlayer2 interface [Windows Media Player],get_stretchToFit method, IWMPPlayer2.get_stretchToFit, IWMPPlayer2::get_stretchToFit, IWMPPlayer2get_stretchToFit, get_stretchToFit, get_stretchToFit method [Windows Media Player], get_stretchToFit method [Windows Media Player],IWMPPlayer2 interface, wmp.iwmpplayer2_get_stretchtofit, wmp/IWMPPlayer2::get_stretchToFit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPPlayer2::get_stretchToFit
 - wmp/IWMPPlayer2::get_stretchToFit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlayer2.get_stretchToFit
---

# IWMPPlayer2::get_stretchToFit


## -description

The <b>get_stretchToFit</b> method retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window when the video window is larger than the dimensions of the video image.

## -parameters

### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether video displayed by the Windows Media Player control automatically resizes.

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

When the <b>VARIANT_BOOL</b> retrieved by <b>get_stretchToFit</b> equals <b>TRUE</b>, the Windows Media Player control maintains the original aspect ratio of the video. If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and bottom or left and right of the video image.

This method applies to the Windows Media Player control only when embedded in a webpage.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-put_stretchtofit">IWMPPlayer2::put_stretchToFit</a>