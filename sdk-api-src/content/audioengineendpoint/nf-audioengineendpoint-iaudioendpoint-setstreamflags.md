---
UID: NF:audioengineendpoint.IAudioEndpoint.SetStreamFlags
title: IAudioEndpoint::SetStreamFlags (audioengineendpoint.h)
description: Sets the stream configuration flags on the audio endpoint.
helpviewer_keywords: ["IAudioEndpoint interface [Remote Desktop Services]","SetStreamFlags method","IAudioEndpoint.SetStreamFlags","IAudioEndpoint::SetStreamFlags","SetStreamFlags","SetStreamFlags method [Remote Desktop Services]","SetStreamFlags method [Remote Desktop Services]","IAudioEndpoint interface","audioengineendpoint/IAudioEndpoint::SetStreamFlags","termserv.iaudioendpoint_setstreamflags"]
old-location: termserv\iaudioendpoint_setstreamflags.htm
tech.root: TermServ
ms.assetid: f6713912-ba7e-4e3e-95d9-8318c40a7042
ms.date: 12/05/2018
ms.keywords: IAudioEndpoint interface [Remote Desktop Services],SetStreamFlags method, IAudioEndpoint.SetStreamFlags, IAudioEndpoint::SetStreamFlags, SetStreamFlags, SetStreamFlags method [Remote Desktop Services], SetStreamFlags method [Remote Desktop Services],IAudioEndpoint interface, audioengineendpoint/IAudioEndpoint::SetStreamFlags, termserv.iaudioendpoint_setstreamflags
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpoint::SetStreamFlags
 - audioengineendpoint/IAudioEndpoint::SetStreamFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.SetStreamFlags
---

# IAudioEndpoint::SetStreamFlags


## -description

The <b>SetStreamFlags</b> method sets the stream configuration flags on the audio endpoint.

## -parameters

### -param streamFlags [in]

A bitwise <b>OR</b> of one or more of the AUDCLNT_STREAMFLAGS_XXX constants.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpoint">IAudioEndpoint</a>