---
UID: NF:oaidl.ICreateTypeInfo.SetFuncAndParamNames
title: ICreateTypeInfo::SetFuncAndParamNames (oaidl.h)
description: Sets the name of a function and the names of its parameters to the specified names.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetFuncAndParamNames method","ICreateTypeInfo.SetFuncAndParamNames","ICreateTypeInfo::SetFuncAndParamNames","SetFuncAndParamNames","SetFuncAndParamNames method [Automation]","SetFuncAndParamNames method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetFuncAndParamNames","automat.icreatetypeinfo_setfuncandparamnames","oaidl/ICreateTypeInfo::SetFuncAndParamNames"]
old-location: automat\icreatetypeinfo_setfuncandparamnames.htm
tech.root: automat
ms.assetid: e3764917-43ea-4151-95da-e01946a2ebb7
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetFuncAndParamNames method, ICreateTypeInfo.SetFuncAndParamNames, ICreateTypeInfo::SetFuncAndParamNames, SetFuncAndParamNames, SetFuncAndParamNames method [Automation], SetFuncAndParamNames method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetFuncAndParamNames, automat.icreatetypeinfo_setfuncandparamnames, oaidl/ICreateTypeInfo::SetFuncAndParamNames
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
 - ICreateTypeInfo::SetFuncAndParamNames
 - oaidl/ICreateTypeInfo::SetFuncAndParamNames
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
 - ICreateTypeInfo.SetFuncAndParamNames
---

# ICreateTypeInfo::SetFuncAndParamNames


## -description

Sets the name of a function and the names of its parameters to the specified names.

## -parameters

### -param index [in]

The index of the function whose function name and parameter names are to be set.

### -param rgszNames [in]

An array of pointers to names. The first element is the function name. Subsequent elements are names of parameters.

### -param cNames [in]

The number of elements in the <i>rgszNames</i> array.

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
<dt><b>S_OK
</b></dt>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The element cannot be found.


</td>
</tr>
</table>

## -remarks

This method must be used once for each property. The last parameter for put and putref accessor functions is unnamed.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>