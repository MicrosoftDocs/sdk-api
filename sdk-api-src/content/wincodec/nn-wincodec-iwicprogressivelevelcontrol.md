---
UID: NN:wincodec.IWICProgressiveLevelControl
title: IWICProgressiveLevelControl (wincodec.h)
author: windows-sdk-content
description: Exposes methods for obtaining information about and controlling progressive decoding.
old-location: wic\_wic_codec_iwicprogressivelevelcontrol.htm
tech.root: wic
ms.assetid: d77244bc-b9d4-4b7d-b718-4ee38de46614
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICProgressiveLevelControl, IWICProgressiveLevelControl interface [Windows Imaging Component], IWICProgressiveLevelControl interface [Windows Imaging Component],described, _wic_codec_iwicprogressivelevelcontrol, wic._wic_codec_iwicprogressivelevelcontrol, wincodec/IWICProgressiveLevelControl
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICProgressiveLevelControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICProgressiveLevelControl interface


## -description


Exposes methods for obtaining information about and controlling progressive decoding.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICProgressiveLevelControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICProgressiveLevelControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICProgressiveLevelControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-getcurrentlevel">GetCurrentLevel</a>
</td>
<td align="left" width="63%">
Gets the last level set by the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel">SetCurrentLevel</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-getlevelcount">GetLevelCount</a>
</td>
<td align="left" width="63%">
Gets the number of levels of progressive decoding supported by the CODEC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel">SetCurrentLevel</a>
</td>
<td align="left" width="63%">
Specifies the level to retrieve on the next call to <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a>.

</td>
</tr>
</table> 


## -remarks



Images can only be progressively decoded if they were progressively encoded. Progressive images automatically start at the highest (best quality) progressive level. The caller must manually set the decoder to a lower progressive level.

E_NOTIMPL is returned if the codec does not support progressive level decoding.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-progressive-decoding">Progressive Decoding Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-sample-progressive-decoding">WIC Progressive Decoding Sample</a>
 

 

