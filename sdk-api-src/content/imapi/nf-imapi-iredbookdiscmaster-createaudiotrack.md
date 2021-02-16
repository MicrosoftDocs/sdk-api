---
UID: NF:imapi.IRedbookDiscMaster.CreateAudioTrack
title: IRedbookDiscMaster::CreateAudioTrack (imapi.h)
description: Begins staging a new audio track. It can be called only when there are no open audio tracks in the image.
helpviewer_keywords: ["CreateAudioTrack","CreateAudioTrack method [IMAPI]","CreateAudioTrack method [IMAPI]","IRedbookDiscMaster interface","IRedbookDiscMaster interface [IMAPI]","CreateAudioTrack method","IRedbookDiscMaster.CreateAudioTrack","IRedbookDiscMaster::CreateAudioTrack","_win32_iredbookdiscmaster_createaudiotrack","base.iredbookdiscmaster_createaudiotrack","imapi.iredbookdiscmaster_createaudiotrack","imapi/IRedbookDiscMaster::CreateAudioTrack"]
old-location: imapi\iredbookdiscmaster_createaudiotrack.htm
tech.root: imapi
ms.assetid: b0300cd8-08e9-434e-9c1b-c33a19148e7e
ms.date: 12/05/2018
ms.keywords: CreateAudioTrack, CreateAudioTrack method [IMAPI], CreateAudioTrack method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],CreateAudioTrack method, IRedbookDiscMaster.CreateAudioTrack, IRedbookDiscMaster::CreateAudioTrack, _win32_iredbookdiscmaster_createaudiotrack, base.iredbookdiscmaster_createaudiotrack, imapi.iredbookdiscmaster_createaudiotrack, imapi/IRedbookDiscMaster::CreateAudioTrack
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRedbookDiscMaster::CreateAudioTrack
 - imapi/IRedbookDiscMaster::CreateAudioTrack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IRedbookDiscMaster.CreateAudioTrack
---

# IRedbookDiscMaster::CreateAudioTrack


## -description

Begins staging a new audio track. It can be called only when there are no open audio tracks in the image.

## -parameters

### -param nBlocks [in]

Number of audio blocks to be added to this track. You can create up to 99 tracks, and the open track may consume all remaining available audio blocks. 




The <i>nBlocks</i> parameter is advisory only. It does not force the track length to this size.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

After the track is open, use the 
<a href="/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks">AddAudioTrackBlocks</a> method to add data to the track.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>