---
UID: NF:oaidl.ITypeInfo.GetVarDesc
title: ITypeInfo::GetVarDesc (oaidl.h)
description: Retrieves a VARDESC structure that describes the specified variable.
helpviewer_keywords: ["GetVarDesc","GetVarDesc method [Automation]","GetVarDesc method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetVarDesc method","ITypeInfo.GetVarDesc","ITypeInfo::GetVarDesc","_oa96_ITypeInfo_GetVarDesc","automat.itypeinfo_getvardesc","oaidl/ITypeInfo::GetVarDesc"]
old-location: automat\itypeinfo_getvardesc.htm
tech.root: automat
ms.assetid: c4226d33-37ec-4e9a-87ce-92c4ff0e6cb3
ms.date: 12/05/2018
ms.keywords: GetVarDesc, GetVarDesc method [Automation], GetVarDesc method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetVarDesc method, ITypeInfo.GetVarDesc, ITypeInfo::GetVarDesc, _oa96_ITypeInfo_GetVarDesc, automat.itypeinfo_getvardesc, oaidl/ITypeInfo::GetVarDesc
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
 - ITypeInfo::GetVarDesc
 - oaidl/ITypeInfo::GetVarDesc
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
 - ITypeInfo.GetVarDesc
---

# ITypeInfo::GetVarDesc


## -description

Retrieves a VARDESC structure that describes the specified variable.

## -parameters

### -param index [in]

The index of the variable whose description is to be returned. The index should be in the range of 0 to 1 less than the number of variables in this type.

### -param ppVarDesc [out]

A VARDESC that describes the specified variable.

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
</table>

## -remarks

To free the VARDESC structure, use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasevardesc">ReleaseVarDesc</a>.



#### Examples

In the following example, the CHECKRESULT function is undefined. Replace this function with your error handling code.


```cpp
CHECKRESULT(ptypeinfo->GetVarDesc(i, &pvardesc));
idMember = pvardesc->memid;
CHECKRESULT(ptypeinfo->GetDocumentation(idMember, &bstrName, NULL, NULL, 
      NULL));
ptypeinfo->ReleaseVarDesc(pvardesc);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>