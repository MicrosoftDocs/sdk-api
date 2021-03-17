---
UID: NF:imapi2.IRawCDImageCreator.get_ExpectedTableOfContents
title: IRawCDImageCreator::get_ExpectedTableOfContents (imapi2.h)
description: Gets the SCSI-form table of contents for the resulting disc.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","get_ExpectedTableOfContents method","IRawCDImageCreator.get_ExpectedTableOfContents","IRawCDImageCreator::get_ExpectedTableOfContents","get_ExpectedTableOfContents","get_ExpectedTableOfContents method [IMAPI]","get_ExpectedTableOfContents method [IMAPI]","IRawCDImageCreator interface","imapi.irawcdimagecreator_get_expectedtableofcontents","imapi2/IRawCDImageCreator::get_ExpectedTableOfContents"]
old-location: imapi\irawcdimagecreator_get_expectedtableofcontents.htm
tech.root: imapi
ms.assetid: ce65b26f-9cf7-4c61-a343-975e5af17f57
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_ExpectedTableOfContents method, IRawCDImageCreator.get_ExpectedTableOfContents, IRawCDImageCreator::get_ExpectedTableOfContents, get_ExpectedTableOfContents, get_ExpectedTableOfContents method [IMAPI], get_ExpectedTableOfContents method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_expectedtableofcontents, imapi2/IRawCDImageCreator::get_ExpectedTableOfContents
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
 - IRawCDImageCreator::get_ExpectedTableOfContents
 - imapi2/IRawCDImageCreator::get_ExpectedTableOfContents
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
 - IRawCDImageCreator.get_ExpectedTableOfContents
---

# IRawCDImageCreator::get_ExpectedTableOfContents


## -description

Gets the SCSI-form table of contents for the resulting disc.

## -parameters

### -param value [out]

The SCSI-form table of contents for the resulting disc. Accuracy of this value depends on <b>IRawCDImageCreator::get_ExpectedTableOfContents</b> being called after all image properties have been set.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method can only be called after at least one track has been added to the image.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>