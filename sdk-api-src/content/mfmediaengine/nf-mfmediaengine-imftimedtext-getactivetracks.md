---
UID: NF:mfmediaengine.IMFTimedText.GetActiveTracks
title: IMFTimedText::GetActiveTracks (mfmediaengine.h)
description: Gets the list of active timed-text tracks in the timed-text component.
old-location: mf\imftimedtext_getactivetracks.htm
tech.root: medfound
ms.assetid: DF9EEFD2-E699-4251-9769-D1F940938D45
ms.date: 12/05/2018
ms.keywords: GetActiveTracks, GetActiveTracks method [Media Foundation], GetActiveTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetActiveTracks method, IMFTimedText.GetActiveTracks, IMFTimedText::GetActiveTracks, mf.imftimedtext_getactivetracks, mfmediaengine/IMFTimedText::GetActiveTracks
ms.topic: method
f1_keywords:
- mfmediaengine/IMFTimedText.GetActiveTracks
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
- IMFTimedText.GetActiveTracks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedText::GetActiveTracks


## -description


Gets the list of active timed-text tracks in the timed-text component.


## -parameters




### -param activeTracks [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a> interface that can enumerate the list of active timed-text tracks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>
 

 

