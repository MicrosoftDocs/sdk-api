---
UID: NF:imapi2.IRawCDImageCreator.get_ResultingImageType
title: IRawCDImageCreator::get_ResultingImageType (imapi2.h)
description: Retrieves the value that specifies the type of image file that will be generated.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_ResultingImageType method","IRawCDImageCreator.get_ResultingImageType","IRawCDImageCreator::get_ResultingImageType","get_ResultingImageType","get_ResultingImageType method [IMAPI]","get_ResultingImageType method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_resultingimagetype","imapi2/IRawCDImageCreator::get_ResultingImageType"]
old-location: imapi\irawcdimagecreator_get_resultingimagetype.htm
tech.root: imapi
ms.assetid: 006486f7-f766-44a1-a088-71035567a75d
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_ResultingImageType method, IRawCDImageCreator.get_ResultingImageType, IRawCDImageCreator::get_ResultingImageType, get_ResultingImageType, get_ResultingImageType method [IMAPI], get_ResultingImageType method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_resultingimagetype, imapi2/IRawCDImageCreator::get_ResultingImageType
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
 - IRawCDImageCreator::get_ResultingImageType
 - imapi2/IRawCDImageCreator::get_ResultingImageType
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
 - IRawCDImageCreator.get_ResultingImageType
---

# IRawCDImageCreator::get_ResultingImageType


## -description

Retrieves the value that specifies the type of image file that will be generated.

## -parameters

### -param value [out]

Pointer to an <a href="/windows/win32/api/imapi2/ne-imapi2-imapi_format2_raw_cd_data_sector_type">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a> enumeration that defines the current type set for the  image file.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_resultingimagetype">IRawCDImageCreator::put_ResultingImageType</a>