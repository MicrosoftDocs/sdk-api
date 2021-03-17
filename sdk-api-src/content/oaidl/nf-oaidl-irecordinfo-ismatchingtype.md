---
UID: NF:oaidl.IRecordInfo.IsMatchingType
title: IRecordInfo::IsMatchingType (oaidl.h)
description: Determines whether the record that is passed in matches that of the current record information.
helpviewer_keywords: ["IRecordInfo interface [Automation]","IsMatchingType method","IRecordInfo.IsMatchingType","IRecordInfo::IsMatchingType","IsMatchingType","IsMatchingType method [Automation]","IsMatchingType method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_IsMatchingType","automat.irecordinfo_ismatchingtype","oaidl/IRecordInfo::IsMatchingType"]
old-location: automat\irecordinfo_ismatchingtype.htm
tech.root: automat
ms.assetid: 3db29912-3864-4750-b255-77dcffe711cf
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],IsMatchingType method, IRecordInfo.IsMatchingType, IRecordInfo::IsMatchingType, IsMatchingType, IsMatchingType method [Automation], IsMatchingType method [Automation],IRecordInfo interface, _oa96_IRecordInfo_IsMatchingType, automat.irecordinfo_ismatchingtype, oaidl/IRecordInfo::IsMatchingType
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
 - IRecordInfo::IsMatchingType
 - oaidl/IRecordInfo::IsMatchingType
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
 - IRecordInfo.IsMatchingType
---

# IRecordInfo::IsMatchingType


## -description

Determines whether the record that is passed in matches that of the current record information.

## -parameters

### -param pRecordInfo [in]

The information of the record.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The record that is passed in matches the current record information.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The record that is passed in does not match the current record information.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>