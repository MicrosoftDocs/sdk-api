---
UID: NF:oaidl.IRecordInfo.RecordClear
title: IRecordInfo::RecordClear (oaidl.h)
description: Releases object references and other values of a record without deallocating the record.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordClear method","IRecordInfo.RecordClear","IRecordInfo::RecordClear","RecordClear","RecordClear method [Automation]","RecordClear method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordClear","automat.irecordinfo_recordclear","oaidl/IRecordInfo::RecordClear"]
old-location: automat\irecordinfo_recordclear.htm
tech.root: automat
ms.assetid: 979b0702-3342-4036-8113-c84728436ab6
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordClear method, IRecordInfo.RecordClear, IRecordInfo::RecordClear, RecordClear, RecordClear method [Automation], RecordClear method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordClear, automat.irecordinfo_recordclear, oaidl/IRecordInfo::RecordClear
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
 - IRecordInfo::RecordClear
 - oaidl/IRecordInfo::RecordClear
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
 - IRecordInfo.RecordClear
---

# IRecordInfo::RecordClear


## -description

Releases object references and other values of a record without deallocating the record.

## -parameters

### -param pvExisting [in]

The record to be cleared.

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

<b>RecordClear</b> releases memory blocks held by VT_PTR or VT_SAFEARRAY instance fields. The caller needs to free the instance fields memory, <b>RecordClear</b> will do nothing if there are no resources held.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>