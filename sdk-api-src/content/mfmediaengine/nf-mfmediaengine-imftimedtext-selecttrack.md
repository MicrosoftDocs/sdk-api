---
UID: NF:mfmediaengine.IMFTimedText.SelectTrack
title: IMFTimedText::SelectTrack
author: windows-sdk-content
description: Selects or deselects a track of text in the timed-text component.
old-location: mf\imftimedtext_selecttrack.htm
old-project: medfound
ms.assetid: 868FE620-6FF3-4623-BB61-B47D0290D005
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFTimedText interface [Media Foundation],SelectTrack method, IMFTimedText.SelectTrack, IMFTimedText::SelectTrack, SelectTrack, SelectTrack method [Media Foundation], SelectTrack method [Media Foundation],IMFTimedText interface, mf.imftimedtext_selecttrack, mfmediaengine/IMFTimedText::SelectTrack
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFTimedText.SelectTrack
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedText::SelectTrack


## -description


Selects or deselects a track of text in the timed-text component.


## -parameters




### -param trackId




### -param selected






#### - dwTrackId [in]

Type: <b>DWORD</b>

The identifier of the track to select.




#### - fSelected [in]

Type: <b>BOOL</b>

Specifies whether to select or deselect a track of text. Specify <b>TRUE</b> to select the track or <b>FALSE</b> to deselect the track. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

