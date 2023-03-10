---
UID: NF:imapi2.IRawCDImageCreator.get_NumberOfExistingTracks
title: IRawCDImageCreator::get_NumberOfExistingTracks (imapi2.h)
description: Retrieves the number of existing audio tracks on the media. (IRawCDImageCreator.get_NumberOfExistingTracks)
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_NumberOfExistingTracks method","IRawCDImageCreator.get_NumberOfExistingTracks","IRawCDImageCreator::get_NumberOfExistingTracks","get_NumberOfExistingTracks","get_NumberOfExistingTracks method [IMAPI]","get_NumberOfExistingTracks method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_numberofexistingtracks","imapi2/IRawCDImageCreator::get_NumberOfExistingTracks"]
old-location: imapi\irawcdimagecreator_get_numberofexistingtracks.htm
tech.root: imapi
ms.assetid: c10053d0-d9c1-4ac0-aa38-71dacf1e4425
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_NumberOfExistingTracks method, IRawCDImageCreator.get_NumberOfExistingTracks, IRawCDImageCreator::get_NumberOfExistingTracks, get_NumberOfExistingTracks, get_NumberOfExistingTracks method [IMAPI], get_NumberOfExistingTracks method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_numberofexistingtracks, imapi2/IRawCDImageCreator::get_NumberOfExistingTracks
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
 - IRawCDImageCreator::get_NumberOfExistingTracks
 - imapi2/IRawCDImageCreator::get_NumberOfExistingTracks
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
 - IRawCDImageCreator.get_NumberOfExistingTracks
---

# IRawCDImageCreator::get_NumberOfExistingTracks


## -description

Retrieves the number of existing audio tracks on the media.

## -parameters

### -param value [out]

Pointer to a <b>LONG</b> value that indicates the number of audio tracks that currently exist on the media.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>
