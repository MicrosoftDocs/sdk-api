---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetShowBackgroundAlways
title: IMFTimedTextStyle::GetShowBackgroundAlways (mfmediaengine.h)
description: Determines whether the style of timed text always shows the background.
helpviewer_keywords: ["GetShowBackgroundAlways","GetShowBackgroundAlways method [Media Foundation]","GetShowBackgroundAlways method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetShowBackgroundAlways method","IMFTimedTextStyle.GetShowBackgroundAlways","IMFTimedTextStyle::GetShowBackgroundAlways","mf.imftimedtextstyle_getshowbackgroundalways","mfmediaengine/IMFTimedTextStyle::GetShowBackgroundAlways"]
old-location: mf\imftimedtextstyle_getshowbackgroundalways.htm
tech.root: mf
ms.assetid: 3FE2327F-542B-45D3-95F4-09CF0CE26403
ms.date: 12/05/2018
ms.keywords: GetShowBackgroundAlways, GetShowBackgroundAlways method [Media Foundation], GetShowBackgroundAlways method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetShowBackgroundAlways method, IMFTimedTextStyle.GetShowBackgroundAlways, IMFTimedTextStyle::GetShowBackgroundAlways, mf.imftimedtextstyle_getshowbackgroundalways, mfmediaengine/IMFTimedTextStyle::GetShowBackgroundAlways
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
 - IMFTimedTextStyle::GetShowBackgroundAlways
 - mfmediaengine/IMFTimedTextStyle::GetShowBackgroundAlways
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
 - IMFTimedTextStyle.GetShowBackgroundAlways
---

# IMFTimedTextStyle::GetShowBackgroundAlways


## -description

Determines whether the style  of timed text always shows the background.

## -parameters

### -param showBackgroundAlways [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether the style  of timed text always shows the background. The variable specifies <b>TRUE</b> if the background is always shown; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>