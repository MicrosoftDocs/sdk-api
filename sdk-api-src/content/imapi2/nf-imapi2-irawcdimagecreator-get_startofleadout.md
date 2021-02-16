---
UID: NF:imapi2.IRawCDImageCreator.get_StartOfLeadout
title: IRawCDImageCreator::get_StartOfLeadout (imapi2.h)
description: Retrieves the value that defines the LBA for the start of the Leadout. This method can be utilized to determine if the image can be written to a piece of media by comparing it against the LastPossibleStartOfLeadout for the media.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_StartOfLeadout method","IRawCDImageCreator.get_StartOfLeadout","IRawCDImageCreator::get_StartOfLeadout","get_StartOfLeadout","get_StartOfLeadout method [IMAPI]","get_StartOfLeadout method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_startofleadout","imapi2/IRawCDImageCreator::get_StartOfLeadout"]
old-location: imapi\irawcdimagecreator_get_startofleadout.htm
tech.root: imapi
ms.assetid: 5bf40179-31f5-453f-a989-4bcd116a45aa
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_StartOfLeadout method, IRawCDImageCreator.get_StartOfLeadout, IRawCDImageCreator::get_StartOfLeadout, get_StartOfLeadout, get_StartOfLeadout method [IMAPI], get_StartOfLeadout method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_startofleadout, imapi2/IRawCDImageCreator::get_StartOfLeadout
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
 - IRawCDImageCreator::get_StartOfLeadout
 - imapi2/IRawCDImageCreator::get_StartOfLeadout
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
 - IRawCDImageCreator.get_StartOfLeadout
---

# IRawCDImageCreator::get_StartOfLeadout


## -description

Retrieves the value that defines the LBA for the start of the Leadout.  This method can be utilized to determine if the image can be written to a piece of media by comparing it against the <b>LastPossibleStartOfLeadout</b> for the media.

## -parameters

### -param value [out]

Pointer to a <b>LONG</b> value that represents the LBA for the start of the Leadout.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

Use of this method requires that at least 1 track has been added to the image.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>