---
UID: NF:imapi2.IRawCDImageCreator.AddSubcodeRWGenerator
title: IRawCDImageCreator::AddSubcodeRWGenerator (imapi2.h)
description: Allows the addition of custom R-W subcode, provided by the IStream. The provided object must have a size equal to the number of sectors in the raw disc image * 96 bytes when the final image is created.
helpviewer_keywords: ["AddSubcodeRWGenerator","AddSubcodeRWGenerator method [IMAPI]","AddSubcodeRWGenerator method [IMAPI]","IRawCDImageCreator interface","IRawCDImageCreator interface [IMAPI]","AddSubcodeRWGenerator method","IRawCDImageCreator.AddSubcodeRWGenerator","IRawCDImageCreator::AddSubcodeRWGenerator","imapi.irawcdimagecreator_addsubcoderwgenerator","imapi2/IRawCDImageCreator::AddSubcodeRWGenerator"]
old-location: imapi\irawcdimagecreator_addsubcoderwgenerator.htm
tech.root: imapi
ms.assetid: b952d31e-812e-41b0-98b0-0f9afbe4b01e
ms.date: 12/05/2018
ms.keywords: AddSubcodeRWGenerator, AddSubcodeRWGenerator method [IMAPI], AddSubcodeRWGenerator method [IMAPI],IRawCDImageCreator interface, IRawCDImageCreator interface [IMAPI],AddSubcodeRWGenerator method, IRawCDImageCreator.AddSubcodeRWGenerator, IRawCDImageCreator::AddSubcodeRWGenerator, imapi.irawcdimagecreator_addsubcoderwgenerator, imapi2/IRawCDImageCreator::AddSubcodeRWGenerator
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
 - IRawCDImageCreator::AddSubcodeRWGenerator
 - imapi2/IRawCDImageCreator::AddSubcodeRWGenerator
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
 - IRawCDImageCreator.AddSubcodeRWGenerator
---

# IRawCDImageCreator::AddSubcodeRWGenerator


## -description

Allows the addition of custom R-W subcode, provided by the <b>IStream</b>. The provided object must  have a size equal to the number of sectors in the raw disc image * 96 bytes when the final image is created.

## -parameters

### -param subcode [in, optional]

The subcode data (with 96 bytes per sector), where the 2 most significant bits must always be zero (as they are the P/Q bits).

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

May be added anytime prior to calling <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage">IRawCDImageCreator::CreateResultImage</a>.  If <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_resultingimagetype">IRawCDImageCreator::put_ResultingImageType</a> is  set to return PQ only, then this call will fail as no RW subcode will be used in the resulting image.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage">IRawCDImageCreator::CreateResultImage</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_resultingimagetype">IRawCDImageCreator::put_ResultingImageType</a>