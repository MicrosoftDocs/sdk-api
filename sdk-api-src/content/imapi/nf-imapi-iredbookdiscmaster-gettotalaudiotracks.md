---
UID: NF:imapi.IRedbookDiscMaster.GetTotalAudioTracks
title: IRedbookDiscMaster::GetTotalAudioTracks (imapi.h)
description: Retrieves the total number of tracks that have either been staged or are being staged.
helpviewer_keywords: ["GetTotalAudioTracks","GetTotalAudioTracks method [IMAPI]","GetTotalAudioTracks method [IMAPI]","IRedbookDiscMaster interface","IRedbookDiscMaster interface [IMAPI]","GetTotalAudioTracks method","IRedbookDiscMaster.GetTotalAudioTracks","IRedbookDiscMaster::GetTotalAudioTracks","_win32_iredbookdiscmaster_gettotalaudiotracks","base.iredbookdiscmaster_gettotalaudiotracks","imapi.iredbookdiscmaster_gettotalaudiotracks","imapi/IRedbookDiscMaster::GetTotalAudioTracks"]
old-location: imapi\iredbookdiscmaster_gettotalaudiotracks.htm
tech.root: imapi
ms.assetid: ef284941-0724-4e0a-8ce9-c47d5a53a30e
ms.date: 12/05/2018
ms.keywords: GetTotalAudioTracks, GetTotalAudioTracks method [IMAPI], GetTotalAudioTracks method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetTotalAudioTracks method, IRedbookDiscMaster.GetTotalAudioTracks, IRedbookDiscMaster::GetTotalAudioTracks, _win32_iredbookdiscmaster_gettotalaudiotracks, base.iredbookdiscmaster_gettotalaudiotracks, imapi.iredbookdiscmaster_gettotalaudiotracks, imapi/IRedbookDiscMaster::GetTotalAudioTracks
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
 - IRedbookDiscMaster::GetTotalAudioTracks
 - imapi/IRedbookDiscMaster::GetTotalAudioTracks
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
 - IRedbookDiscMaster.GetTotalAudioTracks
---

# IRedbookDiscMaster::GetTotalAudioTracks


## -description

Retrieves the total number of tracks that have either been staged or are being staged.

## -parameters

### -param pnTracks [out]

Total number of closed and open tracks.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>