---
UID: NF:imapi.IRedbookDiscMaster.CloseAudioTrack
title: IRedbookDiscMaster::CloseAudioTrack (imapi.h)
description: Closes a currently open audio track. All audio tracks must be closed before the IDiscMaster::RecordDisc method can be called.
helpviewer_keywords: ["CloseAudioTrack","CloseAudioTrack method [IMAPI]","CloseAudioTrack method [IMAPI]","IRedbookDiscMaster interface","IRedbookDiscMaster interface [IMAPI]","CloseAudioTrack method","IRedbookDiscMaster.CloseAudioTrack","IRedbookDiscMaster::CloseAudioTrack","_win32_iredbookdiscmaster_closeaudiotrack","base.iredbookdiscmaster_closeaudiotrack","imapi.iredbookdiscmaster_closeaudiotrack","imapi/IRedbookDiscMaster::CloseAudioTrack"]
old-location: imapi\iredbookdiscmaster_closeaudiotrack.htm
tech.root: imapi
ms.assetid: 01ec0eba-d592-46eb-8029-86cb678b8b34
ms.date: 12/05/2018
ms.keywords: CloseAudioTrack, CloseAudioTrack method [IMAPI], CloseAudioTrack method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],CloseAudioTrack method, IRedbookDiscMaster.CloseAudioTrack, IRedbookDiscMaster::CloseAudioTrack, _win32_iredbookdiscmaster_closeaudiotrack, base.iredbookdiscmaster_closeaudiotrack, imapi.iredbookdiscmaster_closeaudiotrack, imapi/IRedbookDiscMaster::CloseAudioTrack
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
 - IRedbookDiscMaster::CloseAudioTrack
 - imapi/IRedbookDiscMaster::CloseAudioTrack
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
 - IRedbookDiscMaster.CloseAudioTrack
---

# IRedbookDiscMaster::CloseAudioTrack


## -description

Closes a currently open audio track. All audio tracks must be closed before the 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">IDiscMaster::RecordDisc</a> method can be called.



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>
