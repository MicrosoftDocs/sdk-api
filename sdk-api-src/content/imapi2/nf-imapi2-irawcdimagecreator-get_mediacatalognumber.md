---
UID: NF:imapi2.IRawCDImageCreator.get_MediaCatalogNumber
title: IRawCDImageCreator::get_MediaCatalogNumber (imapi2.h)
description: Sets the Media Catalog Number (MCN) for the entire audio disc.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_MediaCatalogNumber method","IRawCDImageCreator.get_MediaCatalogNumber","IRawCDImageCreator::get_MediaCatalogNumber","get_MediaCatalogNumber","get_MediaCatalogNumber method [IMAPI]","get_MediaCatalogNumber method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_mediacatalognumber","imapi2/IRawCDImageCreator::get_MediaCatalogNumber"]
old-location: imapi\irawcdimagecreator_get_mediacatalognumber.htm
tech.root: imapi
ms.assetid: db6f46b7-9965-4b06-a437-bdfdac7d5efa
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_MediaCatalogNumber method, IRawCDImageCreator.get_MediaCatalogNumber, IRawCDImageCreator::get_MediaCatalogNumber, get_MediaCatalogNumber, get_MediaCatalogNumber method [IMAPI], get_MediaCatalogNumber method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_mediacatalognumber, imapi2/IRawCDImageCreator::get_MediaCatalogNumber
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
 - IRawCDImageCreator::get_MediaCatalogNumber
 - imapi2/IRawCDImageCreator::get_MediaCatalogNumber
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
 - IRawCDImageCreator.get_MediaCatalogNumber
---

# IRawCDImageCreator::get_MediaCatalogNumber


## -description

Sets the Media Catalog Number (MCN) for the entire audio disc.

## -parameters

### -param value [out]

Pointer to a <b>BSTR</b> value that represents the current MCN associated with the audio disc.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

The MCN returned by this method is formatted as a 13-digit decimal number and must also be provided by  the <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_mediacatalognumber">IRawCDImageCreator::put_MediaCatalogNumber</a> method  in the same form.  Additionally, the provided a MCN value provided via <b>IRawCDImageCreator::put_MediaCatalogNumber</b>   must have a valid checksum digit (least significant digit), or it will be rejected.  For improved compatibility with scripting, leading zeros may be excluded. For example, "0123456789012" can be expressed as "123456789012".

Please refer to the MMC specification for details regarding the MCN value.  

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_mediacatalognumber">IRawCDImageCreator::put_MediaCatalogNumber</a>