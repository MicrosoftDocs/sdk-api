---
UID: NF:mfmediaengine.IMFTimedText.GetMetadataTracks
title: IMFTimedText::GetMetadataTracks (mfmediaengine.h)
description: Gets the list of the timed-metadata tracks in the timed-text component.
helpviewer_keywords: ["GetMetadataTracks","GetMetadataTracks method [Media Foundation]","GetMetadataTracks method [Media Foundation]","IMFTimedText interface","IMFTimedText interface [Media Foundation]","GetMetadataTracks method","IMFTimedText.GetMetadataTracks","IMFTimedText::GetMetadataTracks","mf.imftimedtext_getmetadatatracks","mfmediaengine/IMFTimedText::GetMetadataTracks"]
old-location: mf\imftimedtext_getmetadatatracks.htm
tech.root: mf
ms.assetid: EA4D12F6-D1F0-4DA9-BF80-22C6965CE396
ms.date: 12/05/2018
ms.keywords: GetMetadataTracks, GetMetadataTracks method [Media Foundation], GetMetadataTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetMetadataTracks method, IMFTimedText.GetMetadataTracks, IMFTimedText::GetMetadataTracks, mf.imftimedtext_getmetadatatracks, mfmediaengine/IMFTimedText::GetMetadataTracks
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
 - IMFTimedText::GetMetadataTracks
 - mfmediaengine/IMFTimedText::GetMetadataTracks
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
 - IMFTimedText.GetMetadataTracks
---

# IMFTimedText::GetMetadataTracks


## -description

Gets the list of the timed-metadata tracks in the timed-text component.

## -parameters

### -param metadataTracks [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a> interface that can enumerate the list of the timed-metadata tracks.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>