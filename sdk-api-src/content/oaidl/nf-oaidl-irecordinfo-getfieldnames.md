---
UID: NF:oaidl.IRecordInfo.GetFieldNames
title: IRecordInfo::GetFieldNames (oaidl.h)
description: Gets the names of the fields of the record.
helpviewer_keywords: ["GetFieldNames","GetFieldNames method [Automation]","GetFieldNames method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetFieldNames method","IRecordInfo.GetFieldNames","IRecordInfo::GetFieldNames","_oa96_IRecordInfo_GetFieldNames","automat.irecordinfo_getfieldnames","oaidl/IRecordInfo::GetFieldNames"]
old-location: automat\irecordinfo_getfieldnames.htm
tech.root: automat
ms.assetid: 1cf4f149-1cdc-4884-887a-0eb44eeab8ff
ms.date: 12/05/2018
ms.keywords: GetFieldNames, GetFieldNames method [Automation], GetFieldNames method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetFieldNames method, IRecordInfo.GetFieldNames, IRecordInfo::GetFieldNames, _oa96_IRecordInfo_GetFieldNames, automat.irecordinfo_getfieldnames, oaidl/IRecordInfo::GetFieldNames
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
 - IRecordInfo::GetFieldNames
 - oaidl/IRecordInfo::GetFieldNames
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
 - IRecordInfo.GetFieldNames
---

# IRecordInfo::GetFieldNames


## -description

Gets the names of the fields of the record.

## -parameters

### -param pcNames [in, out]

The number of names to return.

### -param rgBstrNames [out]

The name of the array of type BSTR.

If the <i>rgBstrNames</i> parameter is NULL, then <i>pcNames</i> is returned with the number of field names. 

It the <i>rgBstrNames</i> parameter is not NULL, then the string names contained in <i>rgBstrNames</i> are returned. If the number of names in <i>pcNames</i> and <i>rgBstrNames</i> are not equal then the lesser number of the two is the number of returned field names. The caller needs to free the BSTRs inside the array returned in <i>rgBstrNames</i>.

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

The caller should allocate memory for the array of BSTRs. If the array is larger than needed, set the unused portion to 0.

On return, the caller will need to free each contained BSTR using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

In case of out of memory, <i>pcNames</i> points to error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>