---
UID: NF:mfmediaengine.IMFTimedTextCue.GetStyle
title: IMFTimedTextCue::GetStyle
author: windows-sdk-content
description: Gets info about the style of the timed-text cue.
old-location: mf\imftimedtextcue_getstyle.htm
tech.root: medfound
ms.assetid: 9E0B570D-69AA-449D-9988-96632A52756F
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetStyle, GetStyle method [Media Foundation], GetStyle method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetStyle method, IMFTimedTextCue.GetStyle, IMFTimedTextCue::GetStyle, mf.imftimedtextcue_getstyle, mfmediaengine/IMFTimedTextCue::GetStyle
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
 - IMFTimedTextCue.GetStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextCue::GetStyle


## -description


Gets info about the style  of the timed-text cue.


## -parameters




### -param style

TBD




#### - ppStyle [out]

Type: <b><a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a> interface for the timed-text style. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

