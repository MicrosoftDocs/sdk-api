---
UID: NF:mfmediaengine.IMFTimedText.GetTextTracks
title: IMFTimedText::GetTextTracks (mfmediaengine.h)
author: windows-sdk-content
description: Gets the list of all the timed-text tracks in the timed-text component.
old-location: mf\imftimedtext_gettexttracks.htm
tech.root: medfound
ms.assetid: 75F2874A-67E0-4167-9B5D-A8B90C3509E0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTextTracks, GetTextTracks method [Media Foundation], GetTextTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetTextTracks method, IMFTimedText.GetTextTracks, IMFTimedText::GetTextTracks, mf.imftimedtext_gettexttracks, mfmediaengine/IMFTimedText::GetTextTracks
ms.topic: method
f1_keywords: ["mfmediaengine/IMFTimedText.GetTextTracks"]
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
 - IMFTimedText.GetTextTracks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedText::GetTextTracks


## -description


Gets the list of all the timed-text tracks in the timed-text component.


## -parameters




### -param textTracks [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a> interface that can enumerate the list of all of the timed-text tracks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>
 

 

