---
UID: NF:mfmediaengine.IMFTimedText.GetTracks
title: IMFTimedText::GetTracks
author: windows-sdk-content
description: Retrieves a list of all timed-text tracks registered with the IMFTimedText.
old-location: mf\imftimedtext_gettracks.htm
tech.root: medfound
ms.assetid: 4ECBC4CD-12A0-493A-A301-1E392F6EC280
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetTracks, GetTracks method [Media Foundation], GetTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetTracks method, IMFTimedText.GetTracks, IMFTimedText::GetTracks, mf.imftimedtext_gettracks, mfmediaengine/IMFTimedText::GetTracks
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
 - IMFTimedText.GetTracks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedText::GetTracks


## -description


Retrieves a list of all timed-text tracks registered with the <a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>.


## -parameters




### -param tracks [out]

Type: <b>IMFTimedTextTrackList**</b>

Receives a pointer to track list.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

