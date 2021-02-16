---
UID: NF:oaidl.IRecordInfo.GetField
title: IRecordInfo::GetField (oaidl.h)
description: Returns a pointer to the VARIANT containing the value of a given field name.
helpviewer_keywords: ["GetField","GetField method [Automation]","GetField method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetField method","IRecordInfo.GetField","IRecordInfo::GetField","_oa96_IRecordInfo_GetField","automat.irecordinfo_getfield","oaidl/IRecordInfo::GetField"]
old-location: automat\irecordinfo_getfield.htm
tech.root: automat
ms.assetid: 6765371c-209a-4794-bff8-83560171affb
ms.date: 12/05/2018
ms.keywords: GetField, GetField method [Automation], GetField method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetField method, IRecordInfo.GetField, IRecordInfo::GetField, _oa96_IRecordInfo_GetField, automat.irecordinfo_getfield, oaidl/IRecordInfo::GetField
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
 - IRecordInfo::GetField
 - oaidl/IRecordInfo::GetField
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
 - IRecordInfo.GetField
---

# IRecordInfo::GetField


## -description

Returns a pointer to the VARIANT containing the value of a given field name.

## -parameters

### -param pvData [in]

The instance of a record.

### -param szFieldName [in]

The field name.

### -param pvarField [out]

The VARIANT that you want to hold the value of the field name, <i>szFieldName</i>. On return, places a copy of the field's value in the variant.

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

The VARIANT that you pass in contains a copy of the field's value upon return. If you modify the VARIANT then the underlying record field does not change.

The caller allocates memory of the VARIANT.

The method <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> is called for <i>pvarField</i> before copying.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>