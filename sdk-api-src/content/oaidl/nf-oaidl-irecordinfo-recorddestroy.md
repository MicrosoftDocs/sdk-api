---
UID: NF:oaidl.IRecordInfo.RecordDestroy
title: IRecordInfo::RecordDestroy (oaidl.h)
description: Releases the resources and deallocates the memory of the record.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordDestroy method","IRecordInfo.RecordDestroy","IRecordInfo::RecordDestroy","RecordDestroy","RecordDestroy method [Automation]","RecordDestroy method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordDestroy","automat.irecordinfo_recorddestroy","oaidl/IRecordInfo::RecordDestroy"]
old-location: automat\irecordinfo_recorddestroy.htm
tech.root: automat
ms.assetid: 36faf2f6-ecb5-4d6f-a05d-a37ae21a8f07
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordDestroy method, IRecordInfo.RecordDestroy, IRecordInfo::RecordDestroy, RecordDestroy, RecordDestroy method [Automation], RecordDestroy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordDestroy, automat.irecordinfo_recorddestroy, oaidl/IRecordInfo::RecordDestroy
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
 - IRecordInfo::RecordDestroy
 - oaidl/IRecordInfo::RecordDestroy
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
 - IRecordInfo.RecordDestroy
---

# IRecordInfo::RecordDestroy


## -description

Releases the resources and deallocates the memory of the record.

## -parameters

### -param pvRecord [in]

An instance of the record to be destroyed.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
</table>

## -remarks

<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordclear">RecordClear</a> is called to release the resources held by the instance of a record without deallocating memory.

<div class="alert"><b>Note</b>  This method can only be called on records allocated through <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreate">RecordCreate</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreatecopy">RecordCreateCopy</a>. If you allocate the record yourself, you cannot call this method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>