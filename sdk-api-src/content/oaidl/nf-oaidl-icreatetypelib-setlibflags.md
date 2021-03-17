---
UID: NF:oaidl.ICreateTypeLib.SetLibFlags
title: ICreateTypeLib::SetLibFlags (oaidl.h)
description: Sets library flags.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetLibFlags method","ICreateTypeLib.SetLibFlags","ICreateTypeLib::SetLibFlags","SetLibFlags","SetLibFlags method [Automation]","SetLibFlags method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetLibFlags","automat.icreatetypelib_setlibflags","oaidl/ICreateTypeLib::SetLibFlags"]
old-location: automat\icreatetypelib_setlibflags.htm
tech.root: automat
ms.assetid: fc72635c-853f-4a0a-9869-263e4aa39b8b
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetLibFlags method, ICreateTypeLib.SetLibFlags, ICreateTypeLib::SetLibFlags, SetLibFlags, SetLibFlags method [Automation], SetLibFlags method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetLibFlags, automat.icreatetypelib_setlibflags, oaidl/ICreateTypeLib::SetLibFlags
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
 - ICreateTypeLib::SetLibFlags
 - oaidl/ICreateTypeLib::SetLibFlags
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
 - ICreateTypeLib.SetLibFlags
---

# ICreateTypeLib::SetLibFlags


## -description

Sets library flags.

## -parameters

### -param uLibFlags [in]

The flags to set.

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

Valid <i>uLibFlags</i> values are listed in <a href="/windows/desktop/api/oaidl/ne-oaidl-libflags">LIBFLAGS</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>