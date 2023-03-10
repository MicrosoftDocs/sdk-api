---
UID: NF:oaidl.IRecordInfo.RecordCreateCopy
title: IRecordInfo::RecordCreateCopy (oaidl.h)
description: Creates a copy of an instance of a record to the specified location.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordCreateCopy method","IRecordInfo.RecordCreateCopy","IRecordInfo::RecordCreateCopy","RecordCreateCopy","RecordCreateCopy method [Automation]","RecordCreateCopy method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordCreateCopy","automat.irecordinfo_recordcreatecopy","oaidl/IRecordInfo::RecordCreateCopy"]
old-location: automat\irecordinfo_recordcreatecopy.htm
tech.root: automat
ms.assetid: 9cc2a46a-ec92-46a7-8b75-8c36598cc441
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordCreateCopy method, IRecordInfo.RecordCreateCopy, IRecordInfo::RecordCreateCopy, RecordCreateCopy, RecordCreateCopy method [Automation], RecordCreateCopy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCreateCopy, automat.irecordinfo_recordcreatecopy, oaidl/IRecordInfo::RecordCreateCopy
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
 - IRecordInfo::RecordCreateCopy
 - oaidl/IRecordInfo::RecordCreateCopy
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
 - IRecordInfo.RecordCreateCopy
---

# IRecordInfo::RecordCreateCopy


## -description

Creates a copy of an instance of a record to the specified location.

## -parameters

### -param pvSource [in]

An instance of the record to be copied.

### -param ppvDest [out]

The new record with data copied from <i>pvSource</i>.

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
<dt><b>E_OUT_OFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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

The records created must be freed by calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recorddestroy">RecordDestroy</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>