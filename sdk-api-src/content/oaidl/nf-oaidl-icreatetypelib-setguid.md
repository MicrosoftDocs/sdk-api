---
UID: NF:oaidl.ICreateTypeLib.SetGuid
title: ICreateTypeLib::SetGuid (oaidl.h)
description: Sets the universal unique identifier (UUID) associated with the type library.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetGuid method","ICreateTypeLib.SetGuid","ICreateTypeLib::SetGuid","SetGuid","SetGuid method [Automation]","SetGuid method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetGuid","automat.icreatetypelib_setguid","oaidl/ICreateTypeLib::SetGuid"]
old-location: automat\icreatetypelib_setguid.htm
tech.root: automat
ms.assetid: c9afbb9e-3f0a-4862-abb6-82631bae759f
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetGuid method, ICreateTypeLib.SetGuid, ICreateTypeLib::SetGuid, SetGuid, SetGuid method [Automation], SetGuid method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetGuid, automat.icreatetypelib_setguid, oaidl/ICreateTypeLib::SetGuid
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
 - ICreateTypeLib::SetGuid
 - oaidl/ICreateTypeLib::SetGuid
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
 - ICreateTypeLib.SetGuid
---

# ICreateTypeLib::SetGuid


## -description

Sets the universal unique identifier (UUID) associated with the type library (Also known as the globally unique identifier (GUID)).

## -parameters

### -param guid [in]

The globally unique identifier to be assigned to the library.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>



<a href="/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language">Type Libraries and the Object Description Language</a>