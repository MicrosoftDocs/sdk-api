---
UID: NF:oaidl.IRecordInfo.RecordCopy
title: IRecordInfo::RecordCopy (oaidl.h)
description: Copies an existing record into the passed in buffer.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordCopy method","IRecordInfo.RecordCopy","IRecordInfo::RecordCopy","RecordCopy","RecordCopy method [Automation]","RecordCopy method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordCopy","automat.irecordinfo_recordcopy","oaidl/IRecordInfo::RecordCopy"]
old-location: automat\irecordinfo_recordcopy.htm
tech.root: automat
ms.assetid: 0e5a57a2-06d1-47b3-8e3c-c8718b550bcb
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordCopy method, IRecordInfo.RecordCopy, IRecordInfo::RecordCopy, RecordCopy, RecordCopy method [Automation], RecordCopy method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCopy, automat.irecordinfo_recordcopy, oaidl/IRecordInfo::RecordCopy
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
 - IRecordInfo::RecordCopy
 - oaidl/IRecordInfo::RecordCopy
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
 - IRecordInfo.RecordCopy
---

# IRecordInfo::RecordCopy


## -description

Copies an existing record into the passed in buffer.

## -parameters

### -param pvExisting [in]

The current record instance.

### -param pvNew [out]

The destination where the record will be copied.

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

<b>RecordCopy</b> will release the resources in the destination first. The caller is responsible for allocating sufficient memory in the destination by calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getsize">GetSize</a> or  <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreate">RecordCreate</a>. If <b>RecordCopy</b> fails to copy any of the fields then all fields will be cleared, as though <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordclear">RecordClear</a> had been called.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>