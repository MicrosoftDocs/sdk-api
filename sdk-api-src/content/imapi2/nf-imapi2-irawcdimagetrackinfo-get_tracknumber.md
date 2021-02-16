---
UID: NF:imapi2.IRawCDImageTrackInfo.get_TrackNumber
title: IRawCDImageTrackInfo::get_TrackNumber (imapi2.h)
description: Retrieves the track number for this track.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","get_TrackNumber method","IRawCDImageTrackInfo.get_TrackNumber","IRawCDImageTrackInfo::get_TrackNumber","get_TrackNumber","get_TrackNumber method [IMAPI]","get_TrackNumber method [IMAPI]","IRawCDImageTrackInfo interface","imapi.irawcdimagetrackinfo_get_tracknumber","imapi2/IRawCDImageTrackInfo::get_TrackNumber"]
old-location: imapi\irawcdimagetrackinfo_get_tracknumber.htm
tech.root: imapi
ms.assetid: ccc84237-3819-45b4-980a-a73669f605fb
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_TrackNumber method, IRawCDImageTrackInfo.get_TrackNumber, IRawCDImageTrackInfo::get_TrackNumber, get_TrackNumber, get_TrackNumber method [IMAPI], get_TrackNumber method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_tracknumber, imapi2/IRawCDImageTrackInfo::get_TrackNumber
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
 - IRawCDImageTrackInfo::get_TrackNumber
 - imapi2/IRawCDImageTrackInfo::get_TrackNumber
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
 - IRawCDImageTrackInfo.get_TrackNumber
---

# IRawCDImageTrackInfo::get_TrackNumber


## -description

Retrieves the track number for this track.

## -parameters

### -param value [out]

The track number for this track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

While this value is often identical to the <b>TrackIndex</b> property, it is possible for pure audio discs to start with a track other than track number 1.  This means that the more general formula is that this value is ( TrackIndex + FirstTrackNumber - 1).

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>