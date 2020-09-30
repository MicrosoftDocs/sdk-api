---
UID: NF:oaidl.IRecordInfo.GetFieldNoCopy
title: IRecordInfo::GetFieldNoCopy (oaidl.h)
description: Returns a pointer to the value of a given field name without copying the value and allocating resources.
helpviewer_keywords: ["GetFieldNoCopy","GetFieldNoCopy method [Automation]","GetFieldNoCopy method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetFieldNoCopy method","IRecordInfo.GetFieldNoCopy","IRecordInfo::GetFieldNoCopy","_oa96_IRecordInfo_GetFieldNoCopy","automat.irecordinfo_getfieldnocopy","oaidl/IRecordInfo::GetFieldNoCopy"]
old-location: automat\irecordinfo_getfieldnocopy.htm
tech.root: automat
ms.assetid: 3775fa60-3f34-402f-a7e5-18a00de384b5
ms.date: 12/05/2018
ms.keywords: GetFieldNoCopy, GetFieldNoCopy method [Automation], GetFieldNoCopy method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetFieldNoCopy method, IRecordInfo.GetFieldNoCopy, IRecordInfo::GetFieldNoCopy, _oa96_IRecordInfo_GetFieldNoCopy, automat.irecordinfo_getfieldnocopy, oaidl/IRecordInfo::GetFieldNoCopy
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
 - IRecordInfo::GetFieldNoCopy
 - oaidl/IRecordInfo::GetFieldNoCopy
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
 - IRecordInfo.GetFieldNoCopy
---

# IRecordInfo::GetFieldNoCopy


## -description

Returns a pointer to the value of a given field name without copying the value and allocating resources.

## -parameters

### -param pvData [in]

The instance of a record.

### -param szFieldName [in]

The name of the field.

### -param pvarField [out]

The VARIANT that will contain the UDT upon return.

### -param ppvDataCArray [out]

 Receives the value of the field upon return.

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

Upon return, the VARIANT you pass contains a direct pointer to the record's field, <i>ppvDataCArray</i>. If you modify the VARIANT, then the underlying record field will change.

The caller allocates memory of the VARIANT, but does not own the memory so cannot free <i>pvarField</i>. This method calls <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> for <i>pvarField</i> before filling in the requested field.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>