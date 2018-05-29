---
UID: NF:mfmediaengine.IMFTimedText.GetMetadataTracks
title: IMFTimedText::GetMetadataTracks
author: windows-sdk-content
description: Gets the list of the timed-metadata tracks in the timed-text component.
old-location: mf\imftimedtext_getmetadatatracks.htm
old-project: medfound
ms.assetid: EA4D12F6-D1F0-4DA9-BF80-22C6965CE396
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetMetadataTracks, GetMetadataTracks method [Media Foundation], GetMetadataTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetMetadataTracks method, IMFTimedText.GetMetadataTracks, IMFTimedText::GetMetadataTracks, mf.imftimedtext_getmetadatatracks, mfmediaengine/IMFTimedText::GetMetadataTracks
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
-	IMFTimedText.GetMetadataTracks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedText::GetMetadataTracks


## -description


Gets the list of the timed-metadata tracks in the timed-text component.


## -parameters




### -param metadataTracks






#### - ppMetadataTracks [out]

Type: <b><a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a> interface that can enumerate the list of the timed-metadata tracks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

