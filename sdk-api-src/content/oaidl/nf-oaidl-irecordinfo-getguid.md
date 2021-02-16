---
UID: NF:oaidl.IRecordInfo.GetGuid
title: IRecordInfo::GetGuid (oaidl.h)
description: Gets the GUID of the record type.
helpviewer_keywords: ["GetGuid","GetGuid method [Automation]","GetGuid method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetGuid method","IRecordInfo.GetGuid","IRecordInfo::GetGuid","_oa96_IRecordInfo_GetGuid","automat.irecordinfo_getguid","oaidl/IRecordInfo::GetGuid"]
old-location: automat\irecordinfo_getguid.htm
tech.root: automat
ms.assetid: e28ed38a-5cd6-4edb-871e-e69283e4d47e
ms.date: 12/05/2018
ms.keywords: GetGuid, GetGuid method [Automation], GetGuid method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetGuid method, IRecordInfo.GetGuid, IRecordInfo::GetGuid, _oa96_IRecordInfo_GetGuid, automat.irecordinfo_getguid, oaidl/IRecordInfo::GetGuid
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
 - IRecordInfo::GetGuid
 - oaidl/IRecordInfo::GetGuid
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
 - IRecordInfo.GetGuid
---

# IRecordInfo::GetGuid


## -description

Gets the GUID of the record type.

## -parameters

### -param pguid [out]

The class GUID of the TypeInfo that describes the UDT.

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
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>