---
UID: NF:imapi2.IRawCDImageTrackInfo.get_SectorCount
title: IRawCDImageTrackInfo::get_SectorCount (imapi2.h)
description: Retrieves the number of user sectors in this track.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","get_SectorCount method","IRawCDImageTrackInfo.get_SectorCount","IRawCDImageTrackInfo::get_SectorCount","get_SectorCount","get_SectorCount method [IMAPI]","get_SectorCount method [IMAPI]","IRawCDImageTrackInfo interface","imapi.irawcdimagetrackinfo_get_sectorcount","imapi2/IRawCDImageTrackInfo::get_SectorCount"]
old-location: imapi\irawcdimagetrackinfo_get_sectorcount.htm
tech.root: imapi
ms.assetid: 1762620b-b429-4674-85e2-f6f206de1a4f
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_SectorCount method, IRawCDImageTrackInfo.get_SectorCount, IRawCDImageTrackInfo::get_SectorCount, get_SectorCount, get_SectorCount method [IMAPI], get_SectorCount method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_sectorcount, imapi2/IRawCDImageTrackInfo::get_SectorCount
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
 - IRawCDImageTrackInfo::get_SectorCount
 - imapi2/IRawCDImageTrackInfo::get_SectorCount
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
 - IRawCDImageTrackInfo.get_SectorCount
---

# IRawCDImageTrackInfo::get_SectorCount


## -description

Retrieves the number of user sectors in this track.

## -parameters

### -param value [out]

The number of user sectors in this track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

The end of the track is typically the <b>StartingLBA</b> plus the <b>SectorCount</b>.  The start of the next track includes both of these properties plus any required pregap or postgap.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>