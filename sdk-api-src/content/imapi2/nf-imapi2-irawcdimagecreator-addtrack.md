---
UID: NF:imapi2.IRawCDImageCreator.AddTrack
title: IRawCDImageCreator::AddTrack (imapi2.h)
description: Accepts the provided IStream object and saves the interface pointer as the next track in the image.
helpviewer_keywords: ["AddTrack","AddTrack method [IMAPI]","AddTrack method [IMAPI]","IRawCDImageCreator interface","IRawCDImageCreator interface [IMAPI]","AddTrack method","IRawCDImageCreator.AddTrack","IRawCDImageCreator::AddTrack","imapi.irawcdimagecreator_addtrack","imapi2/IRawCDImageCreator::AddTrack"]
old-location: imapi\irawcdimagecreator_addtrack.htm
tech.root: imapi
ms.assetid: 913393e8-6d60-4b1a-b482-32225860f714
ms.date: 12/05/2018
ms.keywords: AddTrack, AddTrack method [IMAPI], AddTrack method [IMAPI],IRawCDImageCreator interface, IRawCDImageCreator interface [IMAPI],AddTrack method, IRawCDImageCreator.AddTrack, IRawCDImageCreator::AddTrack, imapi.irawcdimagecreator_addtrack, imapi2/IRawCDImageCreator::AddTrack
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
 - IRawCDImageCreator::AddTrack
 - imapi2/IRawCDImageCreator::AddTrack
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
 - IRawCDImageCreator.AddTrack
---

# IRawCDImageCreator::AddTrack


## -description

Accepts the provided <b>IStream</b> object and saves the interface pointer as the next track in the image.

## -parameters

### -param dataType [in]

A  value, defined by  <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a>, that indicates the type of data. <b>IMAPI_CD_SECTOR_AUDIO</b> is the only value  supported by the <b>IRawCDImageCreator::AddTrack</b>  method.

### -param data [in, optional]

Pointer to the provided <b>IStream</b> object.

### -param trackIndex [out, retval]

A <b>LONG</b> value within a 1 to 99 range that will be associated with the new track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

Any additional tracks must be compatible with all existing tracks.  See the <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a> enumeration for  information on limitations.

The data stream must be at least 4 seconds (300 sectors) long.  Data stream may not cause final sector to exceed LBA 398,099 (MSF 88:29:74), as leadout would then exceed the MSF 89:59:74 maximum.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>