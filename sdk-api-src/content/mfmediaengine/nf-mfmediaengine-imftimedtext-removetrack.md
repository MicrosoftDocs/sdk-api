---
UID: NF:mfmediaengine.IMFTimedText.RemoveTrack
title: IMFTimedText::RemoveTrack (mfmediaengine.h)
author: windows-sdk-content
description: Removes the timed-text track with the specified identifier.
old-location: mf\imftimedtext_removetrack.htm
tech.root: medfound
ms.assetid: 34B785F6-0B34-431A-91CD-3C2DCEFEDAA4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTimedText interface [Media Foundation],RemoveTrack method, IMFTimedText.RemoveTrack, IMFTimedText::RemoveTrack, RemoveTrack, RemoveTrack method [Media Foundation], RemoveTrack method [Media Foundation],IMFTimedText interface, mf.imftimedtext_removetrack, mfmediaengine/IMFTimedText::RemoveTrack
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.dll
api_name:
 - IMFTimedText.RemoveTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedText::RemoveTrack


## -description


Removes the timed-text track with the specified identifier.


## -parameters




### -param track [in]

Type: <b>DWORD</b>

The identifier of the track to remove.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Get the identifier for a track by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getid">GetId</a>. 

When a track is removed, all buffered data from the track is also removed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>
 

 

