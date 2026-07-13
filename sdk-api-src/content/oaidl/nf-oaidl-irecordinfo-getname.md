---
UID: NF:oaidl.IRecordInfo.GetName
title: IRecordInfo::GetName (oaidl.h)
description: Gets the name of the record type.
helpviewer_keywords: ["GetName","GetName method [Automation]","GetName method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetName method","IRecordInfo.GetName","IRecordInfo::GetName","_oa96_IRecordInfo_GetName","automat.irecordinfo_getname","oaidl/IRecordInfo::GetName"]
old-location: automat\irecordinfo_getname.htm
tech.root: automat
ms.assetid: b769f792-45cb-4070-9be7-0b95b17a9ed8
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Automation], GetName method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetName method, IRecordInfo.GetName, IRecordInfo::GetName, _oa96_IRecordInfo_GetName, automat.irecordinfo_getname, oaidl/IRecordInfo::GetName
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
 - IRecordInfo::GetName
 - oaidl/IRecordInfo::GetName
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
 - IRecordInfo.GetName
---

# IRecordInfo::GetName


## -description

Gets the name of the record type. This is useful if you want to print out the type of the record, because each UDT has its own <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>.

## -parameters

### -param pbstrName [out]

The name.

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
</table>

## -remarks

The caller must free the BSTR by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>