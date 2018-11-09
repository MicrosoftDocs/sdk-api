---
UID: NF:mfmediaengine.IMFTimedText.RemoveTrack
title: IMFTimedText::RemoveTrack
author: windows-sdk-content
description: Removes the timed-text track with the specified identifier.
old-location: mf\imftimedtext_removetrack.htm
tech.root: medfound
ms.assetid: 34B785F6-0B34-431A-91CD-3C2DCEFEDAA4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFTimedText interface [Media Foundation],RemoveTrack method, IMFTimedText.RemoveTrack, IMFTimedText::RemoveTrack, RemoveTrack, RemoveTrack method [Media Foundation], RemoveTrack method [Media Foundation],IMFTimedText interface, mf.imftimedtext_removetrack, mfmediaengine/IMFTimedText::RemoveTrack
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IMFTimedText::RemoveTrack


## -description


Removes the timed-text track with the specified identifier.


## -parameters




### -param track

TBD




#### - trackId [in]

Type: <b>DWORD</b>

The identifier of the track to remove.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Get the identifier for a track by calling <a href="https://msdn.microsoft.com/0DDC7864-654E-416B-9EF5-4CD47244E8BE">GetId</a>. 

When a track is removed, all buffered data from the track is also removed.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

