---
UID: NF:mfmediaengine.IMFTimedTextCue.GetLine
title: IMFTimedTextCue::GetLine
author: windows-sdk-content
description: Gets a line of text in the cue from the index of the line.
old-location: mf\imftimedtextcue_getline.htm
tech.root: medfound
ms.assetid: CD29A63D-8D40-43E6-972C-7050E63EA7D3
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetLine, GetLine method [Media Foundation], GetLine method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetLine method, IMFTimedTextCue.GetLine, IMFTimedTextCue::GetLine, mf.imftimedtextcue_getline, mfmediaengine/IMFTimedTextCue::GetLine
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
 - IMFTimedTextCue.GetLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextCue::GetLine


## -description


Gets a line of text in the cue from the index of the line.


## -parameters




### -param index

TBD


### -param line

TBD




#### - nIndex [in]

Type: <b>DWORD</b>

The index of the line of text in the cue to retrieve.




#### - ppLine [out]

Type: <b><a href="https://msdn.microsoft.com/98327CA2-21C4-481F-B979-12C31AA1E7B2">IMFTimedTextFormattedText</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/98327CA2-21C4-481F-B979-12C31AA1E7B2">IMFTimedTextFormattedText</a> interface for the line of text in the cue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

