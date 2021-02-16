---
UID: NF:imapi2.IRawCDImageTrackInfo.get_StartingLba
title: IRawCDImageTrackInfo::get_StartingLba (imapi2.h)
description: Retrieves the LBA of the first user sectors in this track.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","get_StartingLba method","IRawCDImageTrackInfo.get_StartingLba","IRawCDImageTrackInfo::get_StartingLba","get_StartingLba","get_StartingLba method [IMAPI]","get_StartingLba method [IMAPI]","IRawCDImageTrackInfo interface","imapi.irawcdimagetrackinfo_get_startinglba","imapi2/IRawCDImageTrackInfo::get_StartingLba"]
old-location: imapi\irawcdimagetrackinfo_get_startinglba.htm
tech.root: imapi
ms.assetid: 5e1d1404-c52d-4e27-970a-bc1b59995a87
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_StartingLba method, IRawCDImageTrackInfo.get_StartingLba, IRawCDImageTrackInfo::get_StartingLba, get_StartingLba, get_StartingLba method [IMAPI], get_StartingLba method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_startinglba, imapi2/IRawCDImageTrackInfo::get_StartingLba
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
 - IRawCDImageTrackInfo::get_StartingLba
 - imapi2/IRawCDImageTrackInfo::get_StartingLba
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
 - IRawCDImageTrackInfo.get_StartingLba
---

# IRawCDImageTrackInfo::get_StartingLba


## -description

Retrieves the LBA of the first user sectors in this track.

## -parameters

### -param value [out]

The LBA of the first user sectors in this track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

  Most tracks also include a pregap and postgap, which are not included in this value.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDTrackInfo</a>