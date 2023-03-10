---
UID: NF:oaidl.ICreateTypeInfo2.SetName
title: ICreateTypeInfo2::SetName (oaidl.h)
description: Sets the name of the typeinfo.
helpviewer_keywords: ["ICreateTypeInfo2 interface [Automation]","SetName method","ICreateTypeInfo2.SetName","ICreateTypeInfo2::SetName","SetName","SetName method [Automation]","SetName method [Automation]","ICreateTypeInfo2 interface","_oa96_ICreateTypeInfo2_SetName","automat.icreatetypeinfo2_setname","oaidl/ICreateTypeInfo2::SetName"]
old-location: automat\icreatetypeinfo2_setname.htm
tech.root: automat
ms.assetid: b490dcb5-97e4-427a-bc87-22f38a4719f3
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetName method, ICreateTypeInfo2.SetName, ICreateTypeInfo2::SetName, SetName, SetName method [Automation], SetName method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetName, automat.icreatetypeinfo2_setname, oaidl/ICreateTypeInfo2::SetName
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
 - ICreateTypeInfo2::SetName
 - oaidl/ICreateTypeInfo2::SetName
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
 - ICreateTypeInfo2.SetName
---

# ICreateTypeInfo2::SetName


## -description

Sets the name of the typeinfo.

## -parameters

### -param szName [in]

The name to be assigned.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a>