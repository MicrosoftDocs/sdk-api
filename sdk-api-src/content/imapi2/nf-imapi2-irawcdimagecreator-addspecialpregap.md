---
UID: NF:imapi2.IRawCDImageCreator.AddSpecialPregap
title: IRawCDImageCreator::AddSpecialPregap (imapi2.h)
description: Accepts the provided IStream object and saves the associated pointer to be used as data for the pre-gap for track 1.
helpviewer_keywords: ["AddSpecialPregap","AddSpecialPregap method [IMAPI]","AddSpecialPregap method [IMAPI]","IRawCDImageCreator interface","IRawCDImageCreator interface [IMAPI]","AddSpecialPregap method","IRawCDImageCreator.AddSpecialPregap","IRawCDImageCreator::AddSpecialPregap","imapi.irawcdimagecreator_addspecialpregap","imapi2/IRawCDImageCreator::AddSpecialPregap"]
old-location: imapi\irawcdimagecreator_addspecialpregap.htm
tech.root: imapi
ms.assetid: 953ac9e9-b097-4fe5-8bcf-db4f9f15816e
ms.date: 12/05/2018
ms.keywords: AddSpecialPregap, AddSpecialPregap method [IMAPI], AddSpecialPregap method [IMAPI],IRawCDImageCreator interface, IRawCDImageCreator interface [IMAPI],AddSpecialPregap method, IRawCDImageCreator.AddSpecialPregap, IRawCDImageCreator::AddSpecialPregap, imapi.irawcdimagecreator_addspecialpregap, imapi2/IRawCDImageCreator::AddSpecialPregap
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
 - IRawCDImageCreator::AddSpecialPregap
 - imapi2/IRawCDImageCreator::AddSpecialPregap
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
 - IRawCDImageCreator.AddSpecialPregap
---

# IRawCDImageCreator::AddSpecialPregap


## -description

Accepts the provided <b>IStream</b> object and saves the associated pointer to be used as data for the pre-gap for track 1.

## -parameters

### -param data [in, optional]

Pointer to the provided <b>IStream</b> object.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method can only be called prior to adding any tracks to the image.  The <i>data</i> stream must be at least 2 seconds (or 150 sectors) long.

The  <i>data</i> stream should not result final sector exceeding LBA 397,799 (MSF 88:25:74), as the minimal-sized track plus leadout would then exceed the MSF 89:59:74 maximum.  Additionally, it is recommended that the <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a>  value for the first track is implicitly defined as "Audio". The resulting audio can then only be heard by playing the first track and "rewinding" back to the start of the audio disc.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>