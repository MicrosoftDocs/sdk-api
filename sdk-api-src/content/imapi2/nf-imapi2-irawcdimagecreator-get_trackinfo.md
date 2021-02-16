---
UID: NF:imapi2.IRawCDImageCreator.get_TrackInfo
title: IRawCDImageCreator::get_TrackInfo (imapi2.h)
description: Retrieves an indexed property, which takes a LONG value with a range of 1 to 99 as the index to determine which track the user is querying. The returned object is then queried/set for the particular per-track property of interest.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_TrackInfo method","IRawCDImageCreator.get_TrackInfo","IRawCDImageCreator::get_TrackInfo","get_TrackInfo","get_TrackInfo method [IMAPI]","get_TrackInfo method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_trackinfo","imapi2/IRawCDImageCreator::get_TrackInfo"]
old-location: imapi\irawcdimagecreator_get_trackinfo.htm
tech.root: imapi
ms.assetid: e6bc12fe-9274-4339-baf5-80a80512759e
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_TrackInfo method, IRawCDImageCreator.get_TrackInfo, IRawCDImageCreator::get_TrackInfo, get_TrackInfo, get_TrackInfo method [IMAPI], get_TrackInfo method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_trackinfo, imapi2/IRawCDImageCreator::get_TrackInfo
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
 - IRawCDImageCreator::get_TrackInfo
 - imapi2/IRawCDImageCreator::get_TrackInfo
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
 - IRawCDImageCreator.get_TrackInfo
---

# IRawCDImageCreator::get_TrackInfo


## -description

Retrieves an indexed property, which takes a <b>LONG</b> value with a range of 1 to 99 as the index to determine which track the user is querying.  The returned object is then queried/set for the particular per-track property of interest.

## -parameters

### -param trackIndex [in]

A <b>LONG</b> value within a 1 to 99 range that is used to specify which track is  queried.

### -param value [out]

A pointer to a pointer to an <a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a> object that contains information about the track associated with the specified <i>trackInfo</i> index value.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>