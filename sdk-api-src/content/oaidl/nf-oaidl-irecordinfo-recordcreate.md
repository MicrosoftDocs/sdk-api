---
UID: NF:oaidl.IRecordInfo.RecordCreate
title: IRecordInfo::RecordCreate (oaidl.h)
description: Allocates memory for a new record, initializes the instance and returns a pointer to the record.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordCreate method","IRecordInfo.RecordCreate","IRecordInfo::RecordCreate","RecordCreate","RecordCreate method [Automation]","RecordCreate method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordCreate","automat.irecordinfo_recordcreate","oaidl/IRecordInfo::RecordCreate"]
old-location: automat\irecordinfo_recordcreate.htm
tech.root: automat
ms.assetid: f688623e-c03b-456f-bd51-426049e0eb2b
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordCreate method, IRecordInfo.RecordCreate, IRecordInfo::RecordCreate, RecordCreate, RecordCreate method [Automation], RecordCreate method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCreate, automat.irecordinfo_recordcreate, oaidl/IRecordInfo::RecordCreate
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - IRecordInfo::RecordCreate
 - oaidl/IRecordInfo::RecordCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IRecordInfo.RecordCreate
---

# IRecordInfo::RecordCreate


## -description

Allocates memory for a new record, initializes the instance and returns a pointer to the record.



## -returns

This method returns a pointer to the created record.

## -remarks

The memory is set to zeros before it is returned. 

The records created must be freed by calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recorddestroy">RecordDestroy</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>
