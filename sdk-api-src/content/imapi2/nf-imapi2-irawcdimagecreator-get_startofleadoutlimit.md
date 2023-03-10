---
UID: NF:imapi2.IRawCDImageCreator.get_StartOfLeadoutLimit
title: IRawCDImageCreator::get_StartOfLeadoutLimit (imapi2.h)
description: Retrieves the current StartOfLeadoutLimit property value. This value specifies if the resulting image is required to fit on a piece of media with a StartOfLeadout greater than or equal to the LBA.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_StartOfLeadoutLimit method","IRawCDImageCreator.get_StartOfLeadoutLimit","IRawCDImageCreator::get_StartOfLeadoutLimit","get_StartOfLeadoutLimit","get_StartOfLeadoutLimit method [IMAPI]","get_StartOfLeadoutLimit method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_startofleadoutlimit","imapi2/IRawCDImageCreator::get_StartOfLeadoutLimit"]
old-location: imapi\irawcdimagecreator_get_startofleadoutlimit.htm
tech.root: imapi
ms.assetid: 07397f94-fd32-4507-89dd-53de7f25b231
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_StartOfLeadoutLimit method, IRawCDImageCreator.get_StartOfLeadoutLimit, IRawCDImageCreator::get_StartOfLeadoutLimit, get_StartOfLeadoutLimit, get_StartOfLeadoutLimit method [IMAPI], get_StartOfLeadoutLimit method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_startofleadoutlimit, imapi2/IRawCDImageCreator::get_StartOfLeadoutLimit
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
 - IRawCDImageCreator::get_StartOfLeadoutLimit
 - imapi2/IRawCDImageCreator::get_StartOfLeadoutLimit
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
 - IRawCDImageCreator.get_StartOfLeadoutLimit
---

# IRawCDImageCreator::get_StartOfLeadoutLimit


## -description

Retrieves the current <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA.

## -parameters

### -param value [out]

Pointer to a <b>LONG</b> value that represents the current  <i>StartOfLeadoutLimit</i>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_startofleadoutlimit">IRawCDImageCreator::put_StartOfLeadoutLimit</a>