---
UID: NF:mfmediaengine.IMFTimedTextNotify.Cue
title: IMFTimedTextNotify::Cue
author: windows-sdk-content
description: Called when a cue event occurs in a text track.
old-location: mf\imftimedtextnotify_cue.htm
tech.root: medfound
ms.assetid: EE577250-2D75-4130-BA50-95D3E455A574
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Cue, Cue method [Media Foundation], Cue method [Media Foundation],IMFTimedTextNotify interface, IMFTimedTextNotify interface [Media Foundation],Cue method, IMFTimedTextNotify.Cue, IMFTimedTextNotify::Cue, mf.imftimedtextnotify_cue, mfmediaengine/IMFTimedTextNotify::Cue
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
 - IMFTimedTextNotify.Cue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFTimedTextNotify.Cue
: 
---

# IMFTimedTextNotify::Cue


## -description


Called when a cue event occurs in a text track.


## -parameters




### -param cueEvent [in]

Type: <b><a href="https://msdn.microsoft.com/8EA769FD-8BA9-4EBA-96AE-C86720A5F1F1">MF_TIMED_TEXT_CUE_EVENT</a></b>

A value specifying the type of event that has occured.


### -param currentTime [in]

Type: <b>double</b>

The current time when the cue event occurred.


### -param cue [in]

Type: <b><a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>*</b>

The <a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a> object representing the cue.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/FE782D90-8CD4-4F8B-A20E-CE3F792A2DB4">IMFTimedTextNotify</a>
 

 

