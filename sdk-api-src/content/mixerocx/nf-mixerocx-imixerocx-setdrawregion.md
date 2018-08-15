---
UID: NF:mixerocx.IMixerOCX.SetDrawRegion
title: IMixerOCX::SetDrawRegion
author: windows-sdk-content
description: The SetDrawRegion method specifies the location and dimensions of the video and clipping rectangles in screen coordinates.
old-location: dshow\imixerocx_setdrawregion.htm
old-project: DirectShow
ms.assetid: 6f1a9b00-4a35-4772-a185-59b2bc9b9398
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMixerOCX interface [DirectShow],SetDrawRegion method, IMixerOCX.SetDrawRegion, IMixerOCX::SetDrawRegion, IMixerOCXSetDrawRegion, SetDrawRegion, SetDrawRegion method [DirectShow], SetDrawRegion method [DirectShow],IMixerOCX interface, dshow.imixerocx_setdrawregion, mixerocx/IMixerOCX::SetDrawRegion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mixerocx.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>
 

 

