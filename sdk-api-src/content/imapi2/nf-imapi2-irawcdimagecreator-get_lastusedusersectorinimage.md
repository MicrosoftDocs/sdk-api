---
UID: NF:imapi2.IRawCDImageCreator.get_LastUsedUserSectorInImage
title: IRawCDImageCreator::get_LastUsedUserSectorInImage (imapi2.h)
description: Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_LastUsedUserSectorInImage method","IRawCDImageCreator.get_LastUsedUserSectorInImage","IRawCDImageCreator::get_LastUsedUserSectorInImage","get_LastUsedUserSectorInImage","get_LastUsedUserSectorInImage method [IMAPI]","get_LastUsedUserSectorInImage method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_lastusedusersectorinimage","imapi2/IRawCDImageCreator::get_LastUsedUserSectorInImage"]
old-location: imapi\irawcdimagecreator_get_lastusedusersectorinimage.htm
tech.root: imapi
ms.assetid: 4a6b907a-2475-48c8-afd7-e212144bc165
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_LastUsedUserSectorInImage method, IRawCDImageCreator.get_LastUsedUserSectorInImage, IRawCDImageCreator::get_LastUsedUserSectorInImage, get_LastUsedUserSectorInImage, get_LastUsedUserSectorInImage method [IMAPI], get_LastUsedUserSectorInImage method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_lastusedusersectorinimage, imapi2/IRawCDImageCreator::get_LastUsedUserSectorInImage
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
 - IRawCDImageCreator::get_LastUsedUserSectorInImage
 - imapi2/IRawCDImageCreator::get_LastUsedUserSectorInImage
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
 - IRawCDImageCreator.get_LastUsedUserSectorInImage
---

# IRawCDImageCreator::get_LastUsedUserSectorInImage


## -description

Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.

## -parameters

### -param value [out]

Pointer to a <b>LONG</b> value that indicates the number of total used sectors on the media.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This value represents the LBA of the last sector with data that is considered part of a track, and does not include the overhead of the leadin, leadout, or the two-seconds between MSF 00:00:00 and MSF 00:02:00.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>