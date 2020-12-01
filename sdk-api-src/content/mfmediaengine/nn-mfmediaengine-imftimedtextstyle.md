---
UID: NN:mfmediaengine.IMFTimedTextStyle
title: IMFTimedTextStyle (mfmediaengine.h)
description: Represents the style for timed text.
helpviewer_keywords: ["IMFTimedTextStyle","IMFTimedTextStyle interface [Media Foundation]","IMFTimedTextStyle interface [Media Foundation]","described","mf.imftimedtextstyle","mfmediaengine/IMFTimedTextStyle"]
old-location: mf\imftimedtextstyle.htm
tech.root: mf
ms.assetid: ED358A36-BEEF-491E-8984-938F71472F26
ms.date: 12/05/2018
ms.keywords: IMFTimedTextStyle, IMFTimedTextStyle interface [Media Foundation], IMFTimedTextStyle interface [Media Foundation],described, mf.imftimedtextstyle, mfmediaengine/IMFTimedTextStyle
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimedTextStyle
 - mfmediaengine/IMFTimedTextStyle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextStyle
---

# IMFTimedTextStyle interface


## -description

Represents the style for timed text.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextStyle</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedTextStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the background color of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getbold">GetBold</a>
</td>
<td align="left" width="63%">
Determines whether the style  of timed text is bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getcolor">GetColor</a>
</td>
<td align="left" width="63%">
Gets the color of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getfontfamily">GetFontFamily</a>
</td>
<td align="left" width="63%">
Gets the font family of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getfontsize">GetFontSize</a>
</td>
<td align="left" width="63%">
Gets the font size  of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getfontstyle">GetFontStyle</a>
</td>
<td align="left" width="63%">
Gets the font style of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getrighttoleft">GetRightToLeft</a>
</td>
<td align="left" width="63%">
Determines whether the right to left writing mode of the timed-text style  is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-getshowbackgroundalways">GetShowBackgroundAlways</a>
</td>
<td align="left" width="63%">
Determines whether the style  of timed text always shows the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-gettextalignment">GetTextAlignment</a>
</td>
<td align="left" width="63%">
Gets the text alignment of the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-gettextdecoration">GetTextDecoration</a>
</td>
<td align="left" width="63%">
Gets how text is decorated for the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-gettextoutline">GetTextOutline</a>
</td>
<td align="left" width="63%">
Gets the text outline for the timed-text style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextstyle-isexternal">IsExternal</a>
</td>
<td align="left" width="63%">
Determines whether the timed-text style is external.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>