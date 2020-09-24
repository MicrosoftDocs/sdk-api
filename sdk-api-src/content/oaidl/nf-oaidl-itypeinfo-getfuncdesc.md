---
UID: NF:oaidl.ITypeInfo.GetFuncDesc
title: ITypeInfo::GetFuncDesc (oaidl.h)
description: Retrieves the FUNCDESC structure that contains information about a specified function.
helpviewer_keywords: ["GetFuncDesc","GetFuncDesc method [Automation]","GetFuncDesc method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetFuncDesc method","ITypeInfo.GetFuncDesc","ITypeInfo::GetFuncDesc","_oa96_ITypeInfo_GetFuncDesc","automat.itypeinfo_getfuncdesc","oaidl/ITypeInfo::GetFuncDesc"]
old-location: automat\itypeinfo_getfuncdesc.htm
tech.root: automat
ms.assetid: 1e3331a2-0156-4d8f-aa7f-e32cecd3eb74
ms.date: 12/05/2018
ms.keywords: GetFuncDesc, GetFuncDesc method [Automation], GetFuncDesc method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetFuncDesc method, ITypeInfo.GetFuncDesc, ITypeInfo::GetFuncDesc, _oa96_ITypeInfo_GetFuncDesc, automat.itypeinfo_getfuncdesc, oaidl/ITypeInfo::GetFuncDesc
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
 - ITypeInfo::GetFuncDesc
 - oaidl/ITypeInfo::GetFuncDesc
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
 - ITypeInfo.GetFuncDesc
---

# ITypeInfo::GetFuncDesc


## -description

Retrieves the <a href="/windows/desktop/api/oaidl/ns-oaidl-funcdesc">FUNCDESC</a> structure that contains information about a specified function.

## -parameters

### -param index [in]

The index of the function whose description is to be returned. The <i>index</i> should be in the range of 0 to 1 less than the number of functions in this type.

### -param ppFuncDesc [out]

A FUNCDESC structure that describes the specified function.

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

The function <b>ITypeInfo::GetFuncDesc</b> provides access to a FUNCDESC structure that describes the function with the specified <i>index</i>. The FUNCDESC structure should be freed with <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasefuncdesc">ITypeInfo::ReleaseFuncDesc</a>. The number of functions in the type is one of the attributes contained in the TYPEATTR structure.



#### Examples

In the following example, the CHECKRESULT function is undefined. Replace this function with your error handling code.


```cpp
CHECKRESULT(ptypeinfo->GetFuncDesc(i, &pfuncdesc));
idMember = pfuncdesc->memid;
CHECKRESULT(ptypeinfo->GetDocumentation(idMember, &bstrName, NULL, NULL, NULL));
ptypeinfo->ReleaseFuncDesc(pfuncdesc);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>