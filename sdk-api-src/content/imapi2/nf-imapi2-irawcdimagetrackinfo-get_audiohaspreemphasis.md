---
UID: NF:imapi2.IRawCDImageTrackInfo.get_AudioHasPreemphasis
title: IRawCDImageTrackInfo::get_AudioHasPreemphasis (imapi2.h)
description: Retrieves the value that specifies if an audio track has an additional pre-emphasis added to the audio data.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","get_AudioHasPreemphasis method","IRawCDImageTrackInfo.get_AudioHasPreemphasis","IRawCDImageTrackInfo::get_AudioHasPreemphasis","get_AudioHasPreemphasis","get_AudioHasPreemphasis method [IMAPI]","get_AudioHasPreemphasis method [IMAPI]","IRawCDImageTrackInfo interface","imapi.irawcdimagetrackinfo_get_audiohaspreemphasis","imapi2/IRawCDImageTrackInfo::get_AudioHasPreemphasis"]
old-location: imapi\irawcdimagetrackinfo_get_audiohaspreemphasis.htm
tech.root: imapi
ms.assetid: 3e322485-4542-4229-9b3e-17c9774d14b5
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_AudioHasPreemphasis method, IRawCDImageTrackInfo.get_AudioHasPreemphasis, IRawCDImageTrackInfo::get_AudioHasPreemphasis, get_AudioHasPreemphasis, get_AudioHasPreemphasis method [IMAPI], get_AudioHasPreemphasis method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_audiohaspreemphasis, imapi2/IRawCDImageTrackInfo::get_AudioHasPreemphasis
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IRawCDImageTrackInfo::get_AudioHasPreemphasis
 - imapi2/IRawCDImageTrackInfo::get_AudioHasPreemphasis
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo.get_AudioHasPreemphasis
---

# IRawCDImageTrackInfo::get_AudioHasPreemphasis


## -description

Retrieves  the value that specifies if an audio track has an additional pre-emphasis added to the audio data.

## -parameters

### -param value [out]

Value that specifies if an audio track has an additional pre-emphasis added to the audio data.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>