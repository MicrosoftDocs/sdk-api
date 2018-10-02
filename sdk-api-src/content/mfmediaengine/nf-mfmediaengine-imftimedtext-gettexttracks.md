---
UID: NF:mfmediaengine.IMFTimedText.GetTextTracks
title: IMFTimedText::GetTextTracks
author: windows-sdk-content
description: Gets the list of all the timed-text tracks in the timed-text component.
old-location: mf\imftimedtext_gettexttracks.htm
tech.root: MedFound
ms.assetid: 75F2874A-67E0-4167-9B5D-A8B90C3509E0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetTextTracks, GetTextTracks method [Media Foundation], GetTextTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetTextTracks method, IMFTimedText.GetTextTracks, IMFTimedText::GetTextTracks, mf.imftimedtext_gettexttracks, mfmediaengine/IMFTimedText::GetTextTracks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IMFTimedText::GetTextTracks


## -description


Gets the list of all the timed-text tracks in the timed-text component.


## -parameters




### -param textTracks

TBD




#### - ppTextTracks [out]

Type: <b><a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a> interface that can enumerate the list of all of the timed-text tracks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

