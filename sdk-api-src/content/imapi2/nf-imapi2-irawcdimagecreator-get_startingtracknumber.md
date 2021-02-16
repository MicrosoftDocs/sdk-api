---
UID: NF:imapi2.IRawCDImageCreator.get_StartingTrackNumber
title: IRawCDImageCreator::get_StartingTrackNumber (imapi2.h)
description: Retrieves the starting track number.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_StartingTrackNumber method","IRawCDImageCreator.get_StartingTrackNumber","IRawCDImageCreator::get_StartingTrackNumber","get_StartingTrackNumber","get_StartingTrackNumber method [IMAPI]","get_StartingTrackNumber method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_startingtracknumber","imapi2/IRawCDImageCreator::get_StartingTrackNumber"]
old-location: imapi\irawcdimagecreator_get_startingtracknumber.htm
tech.root: imapi
ms.assetid: 307ef0b4-80b2-46c1-acca-1ce5d2222eb7
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_StartingTrackNumber method, IRawCDImageCreator.get_StartingTrackNumber, IRawCDImageCreator::get_StartingTrackNumber, get_StartingTrackNumber, get_StartingTrackNumber method [IMAPI], get_StartingTrackNumber method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_startingtracknumber, imapi2/IRawCDImageCreator::get_StartingTrackNumber
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
 - IRawCDImageCreator::get_StartingTrackNumber
 - imapi2/IRawCDImageCreator::get_StartingTrackNumber
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
 - IRawCDImageCreator.get_StartingTrackNumber
---

# IRawCDImageCreator::get_StartingTrackNumber


## -description

Retrieves the starting track number.

## -parameters

### -param value [out]

Pointer to a <b>LONG</b> value that represents the starting track number.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

If this property holds a  value other than 1, all tracks added to the image must be audio tracks.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_startingtracknumber">IRawCDImageCreator::put_StartingTrackNumber</a>