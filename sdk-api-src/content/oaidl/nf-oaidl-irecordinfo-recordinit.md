---
UID: NF:oaidl.IRecordInfo.RecordInit
title: IRecordInfo::RecordInit (oaidl.h)
description: Initializes a new instance of a record.
helpviewer_keywords: ["IRecordInfo interface [Automation]","RecordInit method","IRecordInfo.RecordInit","IRecordInfo::RecordInit","RecordInit","RecordInit method [Automation]","RecordInit method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_RecordInit","automat.irecordinfo_recordinit","oaidl/IRecordInfo::RecordInit"]
old-location: automat\irecordinfo_recordinit.htm
tech.root: automat
ms.assetid: e10355b3-b751-487d-b7ce-77a39803c38c
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],RecordInit method, IRecordInfo.RecordInit, IRecordInfo::RecordInit, RecordInit, RecordInit method [Automation], RecordInit method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordInit, automat.irecordinfo_recordinit, oaidl/IRecordInfo::RecordInit
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
 - IRecordInfo::RecordInit
 - oaidl/IRecordInfo::RecordInit
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
 - IRecordInfo.RecordInit
---

# IRecordInfo::RecordInit


## -description

Initializes a new instance of a record.

## -parameters

### -param pvNew [out]

An instance of a record.

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

The caller must allocate the memory of the record by its appropriate size using the <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-getsize">GetSize</a> method.

<b>RecordInit</b> sets all contents of the record to 0 and the record should hold no resources.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>