---
UID: NF:mfmediaengine.IMFTimedText.GetActiveTracks
title: IMFTimedText::GetActiveTracks
author: windows-sdk-content
description: Gets the list of active timed-text tracks in the timed-text component.
old-location: mf\imftimedtext_getactivetracks.htm
tech.root: medfound
ms.assetid: DF9EEFD2-E699-4251-9769-D1F940938D45
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetActiveTracks, GetActiveTracks method [Media Foundation], GetActiveTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetActiveTracks method, IMFTimedText.GetActiveTracks, IMFTimedText::GetActiveTracks, mf.imftimedtext_getactivetracks, mfmediaengine/IMFTimedText::GetActiveTracks
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
 - IMFTimedText.GetActiveTracks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedText::GetActiveTracks


## -description


Gets the list of active timed-text tracks in the timed-text component.


## -parameters




### -param activeTracks

TBD




#### - ppActiveTracks [out]

Type: <b><a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a> interface that can enumerate the list of active timed-text tracks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

