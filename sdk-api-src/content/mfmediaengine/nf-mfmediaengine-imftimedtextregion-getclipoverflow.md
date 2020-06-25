---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetClipOverflow
title: IMFTimedTextRegion::GetClipOverflow (mfmediaengine.h)
description: Determines whether a clip of text overflowed the region.
helpviewer_keywords: ["GetClipOverflow","GetClipOverflow method [Media Foundation]","GetClipOverflow method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetClipOverflow method","IMFTimedTextRegion.GetClipOverflow","IMFTimedTextRegion::GetClipOverflow","mf.imftimedtextregion_getclipoverflow","mfmediaengine/IMFTimedTextRegion::GetClipOverflow"]
old-location: mf\imftimedtextregion_getclipoverflow.htm
tech.root: medfound
ms.assetid: F48D4F1C-E00C-40BE-B292-B92C5B214F56
ms.date: 12/05/2018
ms.keywords: GetClipOverflow, GetClipOverflow method [Media Foundation], GetClipOverflow method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetClipOverflow method, IMFTimedTextRegion.GetClipOverflow, IMFTimedTextRegion::GetClipOverflow, mf.imftimedtextregion_getclipoverflow, mfmediaengine/IMFTimedTextRegion::GetClipOverflow
f1_keywords:
- mfmediaengine/IMFTimedTextRegion.GetClipOverflow
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFTimedTextRegion.GetClipOverflow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextRegion::GetClipOverflow


## -description


Determines whether a clip of text overflowed the region.


## -parameters




### -param clipOverflow [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether a clip of text overflowed the region. The variable specifies <b>TRUE</b> if the clip overflowed; otherwise, <b>FALSE</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>
 

 

