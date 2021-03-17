---
UID: NF:oaidl.ICreateTypeLib.SetLcid
title: ICreateTypeLib::SetLcid (oaidl.h)
description: Sets the binary Microsoft national language ID associated with the library.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetLcid method","ICreateTypeLib.SetLcid","ICreateTypeLib::SetLcid","SetLcid","SetLcid method [Automation]","SetLcid method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetLcid","automat.icreatetypelib_setlcid","oaidl/ICreateTypeLib::SetLcid"]
old-location: automat\icreatetypelib_setlcid.htm
tech.root: automat
ms.assetid: 4281058b-a617-4504-bc36-b18763b40897
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetLcid method, ICreateTypeLib.SetLcid, ICreateTypeLib::SetLcid, SetLcid, SetLcid method [Automation], SetLcid method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetLcid, automat.icreatetypelib_setlcid, oaidl/ICreateTypeLib::SetLcid
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
 - ICreateTypeLib::SetLcid
 - oaidl/ICreateTypeLib::SetLcid
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
 - ICreateTypeLib.SetLcid
---

# ICreateTypeLib::SetLcid


## -description

Sets the binary Microsoft national language ID associated with the library.

## -parameters

### -param lcid [in]

The locale ID for the type library.

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

## -remarks

For more information on national language IDs, see <a href="/previous-versions/windows/desktop/automat/supporting-multiple-national-languages">Supporting Multiple National Languages</a> and the National Language Support (NLS) API.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>