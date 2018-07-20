---
UID: NF:mfplay.MFPCreateMediaPlayer
title: MFPCreateMediaPlayer function
author: windows-sdk-content
description: Creates a new instance of the MFPlay player object.
old-location: mf\mfpcreatemediaplayer.htm
old-project: medfound
ms.assetid: 80c668e2-5e93-4af2-871c-646228e18717
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: MFPCreateMediaPlayer, MFPCreateMediaPlayer function [Media Foundation], mf.mfpcreatemediaplayer, mfplay/MFPCreateMediaPlayer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplay.dll
api_name:
 - MFPCreateMediaPlayer
product: Windows
targetos: Windows
req.lib: Mfplay.lib
req.dll: Mfplay.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFPCreateMediaPlayer function


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Creates a new instance of the MFPlay player object.


## -parameters




### -param pwszURL [in]

Null-terminated string that contains the URL  of a media file to open. This parameter can be <b>NULL</b>. If the parameter is <b>NULL</b>, <i>fStartPlayback</i> must be <b>FALSE</b>.

If this parameter is <b>NULL</b>, you can open a URL later by calling <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a>.


### -param fStartPlayback [in]

If <b>TRUE</b>, playback starts automatically. If <b>FALSE</b>, playback does not start until the application calls <a href="https://msdn.microsoft.com/24d6e8a0-d910-46f9-8172-dfcb68c4f364">IMFMediaPlayer::Play</a>.

If <i>pwszURL</i> is <b>NULL</b>, this parameter is ignored.


### -param creationOptions [in]

Bitwise <b>OR</b> of zero of more flags from the <a href="https://msdn.microsoft.com/e01b402c-e21e-4db0-b933-5a32fdca5d2f">_MFP_CREATION_OPTIONS</a> enumeration.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a> interface of a callback object, implemented by the application. Use this interface to get event notifications from the MFPlay player object. This parameter can be <b>NULL</b>. If  the parameter is <b>NULL</b>, the application will not receive  event notifications from the player object.


### -param hWnd [in]

A handle to a window where the video will appear. For audio-only playback, this parameter can be <b>NULL</b>.

The window specified by <i>hWnd</i> is used for the first selected video stream in the source. If the source has multiple video streams, you must call <a href="https://msdn.microsoft.com/97ed9cc0-5f69-4ecb-98c7-c58130b91d7c">IMFPMediaItem::SetStreamSink</a> to render any of the video streams after the first.

If <i>hWnd</i> is <b>NULL</b>, MFPlay will not display any video unless the application calls <a href="https://msdn.microsoft.com/97ed9cc0-5f69-4ecb-98c7-c58130b91d7c">IMFPMediaItem::SetStreamSink</a> to specify a media sink for the video stream. 


### -param ppMediaPlayer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> interface. The caller must release the interface. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, <i>fStartPlayback</i> must be <b>TRUE</b> and <i>pwszURL</i> cannot be <b>NULL</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this function, call <b>CoIntialize(Ex)</b> from the same thread to initialize the COM library.

Internally, <b>MFPCreateMediaPlayer</b> calls <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> to initialize the Microsoft Media Foundation platform. When the player object is destroyed, it calls  <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> to shut down the platform. It is not necessary for an application to call <b>MFStartup</b> or <b>MFShutdown</b> when using MFPlay.

<div class="alert"><b>Note</b>  If you use other Media Foundation APIs outside the life time of the player object, then your application should call <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> and <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

