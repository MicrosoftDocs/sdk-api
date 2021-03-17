---
UID: NF:imapi2.IRawCDImageTrackInfo.put_AudioHasPreemphasis
title: IRawCDImageTrackInfo::put_AudioHasPreemphasis (imapi2.h)
description: Sets the value that specifies if an audio track has an additional pre-emphasis added to the audio data prior to being written to CD.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","put_AudioHasPreemphasis method","IRawCDImageTrackInfo.put_AudioHasPreemphasis","IRawCDImageTrackInfo::put_AudioHasPreemphasis","imapi.irawcdimagetrackinfo_put_audiohaspreemphasis","imapi2/IRawCDImageTrackInfo::put_AudioHasPreemphasis","put_AudioHasPreemphasis","put_AudioHasPreemphasis method [IMAPI]","put_AudioHasPreemphasis method [IMAPI]","IRawCDImageTrackInfo interface"]
old-location: imapi\irawcdimagetrackinfo_put_audiohaspreemphasis.htm
tech.root: imapi
ms.assetid: 60b1d577-2eb7-4767-94ee-03df465234e9
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],put_AudioHasPreemphasis method, IRawCDImageTrackInfo.put_AudioHasPreemphasis, IRawCDImageTrackInfo::put_AudioHasPreemphasis, imapi.irawcdimagetrackinfo_put_audiohaspreemphasis, imapi2/IRawCDImageTrackInfo::put_AudioHasPreemphasis, put_AudioHasPreemphasis, put_AudioHasPreemphasis method [IMAPI], put_AudioHasPreemphasis method [IMAPI],IRawCDImageTrackInfo interface
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
 - IRawCDImageTrackInfo::put_AudioHasPreemphasis
 - imapi2/IRawCDImageTrackInfo::put_AudioHasPreemphasis
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
 - IRawCDImageTrackInfo.put_AudioHasPreemphasis
---

# IRawCDImageTrackInfo::put_AudioHasPreemphasis


## -description

Sets the value that specifies if an audio track has an additional pre-emphasis added to the audio data prior to being written to CD.

## -parameters

### -param value [in]

Value that specifies if an audio track has an additional pre-emphasis added to the audio data.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>