---
UID: NF:imapi2.IRawCDImageCreator.put_StartingTrackNumber
title: IRawCDImageCreator::put_StartingTrackNumber (imapi2.h)
description: Sets the starting track number.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","put_StartingTrackNumber method","IRawCDImageCreator.put_StartingTrackNumber","IRawCDImageCreator::put_StartingTrackNumber","imapi.irawcdimagecreator_put_startingtracknumber","imapi2/IRawCDImageCreator::put_StartingTrackNumber","put_StartingTrackNumber","put_StartingTrackNumber method [IMAPI]","put_StartingTrackNumber method [IMAPI]","IRawCDImageCreator interface"]
old-location: imapi\irawcdimagecreator_put_startingtracknumber.htm
tech.root: imapi
ms.assetid: 38d1319b-0350-41bf-8984-fbeb4f5f3204
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],put_StartingTrackNumber method, IRawCDImageCreator.put_StartingTrackNumber, IRawCDImageCreator::put_StartingTrackNumber, imapi.irawcdimagecreator_put_startingtracknumber, imapi2/IRawCDImageCreator::put_StartingTrackNumber, put_StartingTrackNumber, put_StartingTrackNumber method [IMAPI], put_StartingTrackNumber method [IMAPI],IRawCDImageCreator interface
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
 - IRawCDImageCreator::put_StartingTrackNumber
 - imapi2/IRawCDImageCreator::put_StartingTrackNumber
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
 - IRawCDImageCreator.put_StartingTrackNumber
---

# IRawCDImageCreator::put_StartingTrackNumber


## -description

Sets the starting track number.

## -parameters

### -param value [in]

A <b>LONG</b> value that represents the starting track number.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This property value can only be set before the addition of tracks.  If this property is set to a value other than 1, all tracks added to the image must be audio tracks.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_startingtracknumber">IRawCDImageCreator::get_StartingTrackNumber</a>