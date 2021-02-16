---
UID: NF:oaidl.IRecordInfo.PutField
title: IRecordInfo::PutField (oaidl.h)
description: Puts a variant into a field.
helpviewer_keywords: ["IRecordInfo interface [Automation]","PutField method","IRecordInfo.PutField","IRecordInfo::PutField","PutField","PutField method [Automation]","PutField method [Automation]","IRecordInfo interface","_oa96_IRecordInfo_PutField","automat.irecordinfo_putfield","oaidl/IRecordInfo::PutField"]
old-location: automat\irecordinfo_putfield.htm
tech.root: automat
ms.assetid: 784bb283-b381-405e-b793-d070105b778f
ms.date: 12/05/2018
ms.keywords: IRecordInfo interface [Automation],PutField method, IRecordInfo.PutField, IRecordInfo::PutField, PutField, PutField method [Automation], PutField method [Automation],IRecordInfo interface, _oa96_IRecordInfo_PutField, automat.irecordinfo_putfield, oaidl/IRecordInfo::PutField
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
 - IRecordInfo::PutField
 - oaidl/IRecordInfo::PutField
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
 - IRecordInfo.PutField
---

# IRecordInfo::PutField


## -description

Puts a variant into a field.

## -parameters

### -param wFlags [in]

The only legal values for the wFlags parameter is INVOKE_PROPERTYPUT or INVOKE_PROPERTYPUTREF.

If INVOKE_PROPERTYPUTREF is passed in then <b>PutField</b> just assigns the value of the variant that is passed in to the field using normal coercion rules.

If INVOKE_PROPERTYPUT is passed in then specific rules apply. If the field is declared as a class that derives from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and the field's value is NULL then an error will be returned. If the field's value is not NULL then the variant will be passed to the default property supported by the object referenced by the field. If the field is not declared as a class derived from <b>IDispatch</b> then an error will be returned. If the field is declared as a variant of type VT_Dispatch then the default value of the object is assigned to the field. Otherwise, the variant's value is assigned to the field.

### -param pvData [in, out]

The pointer to an instance of the record.

### -param szFieldName [in]

The name of the field of the record.

### -param pvarField [in]

The pointer to the variant.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>