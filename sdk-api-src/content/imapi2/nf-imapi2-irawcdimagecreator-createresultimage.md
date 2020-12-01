---
UID: NF:imapi2.IRawCDImageCreator.CreateResultImage
title: IRawCDImageCreator::CreateResultImage (imapi2.h)
description: Creates the final IStream object based on the current settings.
helpviewer_keywords: ["CreateResultImage","CreateResultImage method [IMAPI]","CreateResultImage method [IMAPI]","IRawCDImageCreator interface","IRawCDImageCreator interface [IMAPI]","CreateResultImage method","IRawCDImageCreator.CreateResultImage","IRawCDImageCreator::CreateResultImage","imapi.irawcdimagecreator_createresultimage","imapi2/IRawCDImageCreator::CreateResultImage"]
old-location: imapi\irawcdimagecreator_createresultimage.htm
tech.root: imapi
ms.assetid: a83293f6-d5a1-49e2-884b-2b185516109d
ms.date: 12/05/2018
ms.keywords: CreateResultImage, CreateResultImage method [IMAPI], CreateResultImage method [IMAPI],IRawCDImageCreator interface, IRawCDImageCreator interface [IMAPI],CreateResultImage method, IRawCDImageCreator.CreateResultImage, IRawCDImageCreator::CreateResultImage, imapi.irawcdimagecreator_createresultimage, imapi2/IRawCDImageCreator::CreateResultImage
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
 - IRawCDImageCreator::CreateResultImage
 - imapi2/IRawCDImageCreator::CreateResultImage
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
 - IRawCDImageCreator.CreateResultImage
---

# IRawCDImageCreator::CreateResultImage


## -description

Creates the final <b>IStream</b> object based on the current settings.

## -parameters

### -param resultStream [out, optional]

Pointer to the finalized IStream object.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

<b>IRawCDImageCreator::CreateResultImage</b> can only be called once, and will result in the object becoming read-only. All properties associated with this object can  be read but not modified.  The resulting <b>IStream</b> object will be a disc image which starts at MSF 95:00:00, to allow writing of a single image to media with multiple starting addresses.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>