---
UID: NF:imapi.IRedbookDiscMaster.AddAudioTrackBlocks
title: IRedbookDiscMaster::AddAudioTrackBlocks (imapi.h)
description: Adds blocks of audio data to the currently open track. This method can be called repeatedly until there is no space available or the track is full.
helpviewer_keywords: ["AddAudioTrackBlocks","AddAudioTrackBlocks method [IMAPI]","AddAudioTrackBlocks method [IMAPI]","IRedbookDiscMaster interface","IRedbookDiscMaster interface [IMAPI]","AddAudioTrackBlocks method","IRedbookDiscMaster.AddAudioTrackBlocks","IRedbookDiscMaster::AddAudioTrackBlocks","_win32_iredbookdiscmaster_addaudiotrackblocks","base.iredbookdiscmaster_addaudiotrackblocks","imapi.iredbookdiscmaster_addaudiotrackblocks","imapi/IRedbookDiscMaster::AddAudioTrackBlocks"]
old-location: imapi\iredbookdiscmaster_addaudiotrackblocks.htm
tech.root: imapi
ms.assetid: d9bd4f3c-4ff5-4f6e-9520-27fef3736636
ms.date: 12/05/2018
ms.keywords: AddAudioTrackBlocks, AddAudioTrackBlocks method [IMAPI], AddAudioTrackBlocks method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],AddAudioTrackBlocks method, IRedbookDiscMaster.AddAudioTrackBlocks, IRedbookDiscMaster::AddAudioTrackBlocks, _win32_iredbookdiscmaster_addaudiotrackblocks, base.iredbookdiscmaster_addaudiotrackblocks, imapi.iredbookdiscmaster_addaudiotrackblocks, imapi/IRedbookDiscMaster::AddAudioTrackBlocks
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
 - IRedbookDiscMaster::AddAudioTrackBlocks
 - imapi/IRedbookDiscMaster::AddAudioTrackBlocks
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
 - IRedbookDiscMaster.AddAudioTrackBlocks
---

# IRedbookDiscMaster::AddAudioTrackBlocks


## -description

Adds blocks of audio data to the currently open track. This method can be called repeatedly until there is no space available or the track is full.

## -parameters

### -param pby [in]

Pointer to an array of track blocks. The format is 44.1 KHz 16-bit stereo RAW audio samples, in the same format as used by WAV in the data section.

### -param cb [in]

Size of the array, in bytes. This count must be a multiple of the audio block size.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

After all blocks are added, call the 
<a href="/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack">CloseAudioTrack</a> method to finish the track.

If a call to this method would overrun the number of available audio blocks, then the method will return IMAPI_E_DISCFULL and keep as much of the audio data as it can. In contrast, the 
<a href="/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-adddata">IJolietDiscMaster::AddData</a> method does not keep any of the data, so there are no bad files.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>