---
UID: NN:imapi2.IRawCDImageCreator
title: IRawCDImageCreator (imapi2.h)
description: Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the IDiscFormat2RawCD interface.
helpviewer_keywords: ["IRawCDImageCreator","IRawCDImageCreator interface [IMAPI]","IRawCDImageCreator interface [IMAPI]","described","imapi.irawcdimagecreator","imapi2/IRawCDImageCreator"]
old-location: imapi\irawcdimagecreator.htm
tech.root: imapi
ms.assetid: b5fe1a32-545e-417d-9996-34d12862a0ea
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator, IRawCDImageCreator interface [IMAPI], IRawCDImageCreator interface [IMAPI],described, imapi.irawcdimagecreator, imapi2/IRawCDImageCreator
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
 - IRawCDImageCreator
 - imapi2/IRawCDImageCreator
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
 - IRawCDImageCreator
---

# IRawCDImageCreator interface


## -description

Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface. 

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftRawCDImageCreator) for the class identifier and __uuidof(IRawCDImageCreator) for the interface identifier.

## -inheritance

The <b>IRawCDImageCreator</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRawCDImageCreator</b> also has these types of members:

## -remarks

Images created with this interface can be written to persistent storage for later use, or can be provided directly to the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface for writing to CD media.

DVD media does not support this type of writing.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a>
