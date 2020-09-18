---
UID: NF:imapi2.IRawCDImageTrackInfo.put_ISRC
title: IRawCDImageTrackInfo::put_ISRC (imapi2.h)
description: Sets the International Standard Recording Code (ISRC) currently associated with the track. This property value defaults to NULL (or a zero-length string) and may only be set for tracks containing audio data.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","put_ISRC method","IRawCDImageTrackInfo.put_ISRC","IRawCDImageTrackInfo::put_ISRC","imapi.irawcdimagetrackinfo_put_isrc","imapi2/IRawCDImageTrackInfo::put_ISRC","put_ISRC","put_ISRC method [IMAPI]","put_ISRC method [IMAPI]","IRawCDImageTrackInfo interface"]
old-location: imapi\irawcdimagetrackinfo_put_isrc.htm
tech.root: imapi
ms.assetid: c94357dc-9d9f-40a7-8709-51f8d5bc09e5
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],put_ISRC method, IRawCDImageTrackInfo.put_ISRC, IRawCDImageTrackInfo::put_ISRC, imapi.irawcdimagetrackinfo_put_isrc, imapi2/IRawCDImageTrackInfo::put_ISRC, put_ISRC, put_ISRC method [IMAPI], put_ISRC method [IMAPI],IRawCDImageTrackInfo interface
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
 - IRawCDImageTrackInfo::put_ISRC
 - imapi2/IRawCDImageTrackInfo::put_ISRC
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
 - IRawCDImageTrackInfo.put_ISRC
---

# IRawCDImageTrackInfo::put_ISRC


## -description

Sets the International Standard Recording Code (ISRC) currently associated with the track.  This property value defaults to <b>NULL</b> (or a zero-length string) and may only be set for tracks containing audio data.

## -parameters

### -param value [in]

The ISRC to associate with the track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

  The format of the ISRC is provided to the caller formatted per ISRC standards (DIN-31-621) recommendations, such as "US-K7Y-98-12345".  When set, the provided string may optionally exclude all the '-' characters.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>