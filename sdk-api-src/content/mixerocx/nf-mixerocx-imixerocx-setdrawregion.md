---
UID: NF:mixerocx.IMixerOCX.SetDrawRegion
title: IMixerOCX::SetDrawRegion (mixerocx.h)
description: The SetDrawRegion method specifies the location and dimensions of the video and clipping rectangles in screen coordinates.
helpviewer_keywords: ["IMixerOCX interface [DirectShow]","SetDrawRegion method","IMixerOCX.SetDrawRegion","IMixerOCX::SetDrawRegion","IMixerOCXSetDrawRegion","SetDrawRegion","SetDrawRegion method [DirectShow]","SetDrawRegion method [DirectShow]","IMixerOCX interface","dshow.imixerocx_setdrawregion","mixerocx/IMixerOCX::SetDrawRegion"]
old-location: dshow\imixerocx_setdrawregion.htm
tech.root: dshow
ms.assetid: 6f1a9b00-4a35-4772-a185-59b2bc9b9398
ms.date: 12/05/2018
ms.keywords: IMixerOCX interface [DirectShow],SetDrawRegion method, IMixerOCX.SetDrawRegion, IMixerOCX::SetDrawRegion, IMixerOCXSetDrawRegion, SetDrawRegion, SetDrawRegion method [DirectShow], SetDrawRegion method [DirectShow],IMixerOCX interface, dshow.imixerocx_setdrawregion, mixerocx/IMixerOCX::SetDrawRegion
f1_keywords:
- mixerocx/IMixerOCX.SetDrawRegion
dev_langs:
- c++
req.header: mixerocx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMixerOCX.SetDrawRegion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerOCX::SetDrawRegion


## -description



The <code>SetDrawRegion</code> method specifies the location and dimensions of the video and clipping rectangles in screen coordinates.




## -parameters




### -param lpptTopLeftSC [in]

Specifies the top left of the video rectangle in screen coordinates. (The Overlay Mixer filter ignores this parameter. This parameter should be set to <b>NULL</b>.)


### -param prcDrawCC [in]

Specifies the video rectangle in screen coordinates. This parameter cannot be <b>NULL</b>.


### -param lprcClip [in]

Specifies the clipping rectangle in screen coordinates. This parameter cannot be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Either <i>prcDrawCC</i> or <i>lprcClip</i> are <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>
 

 

