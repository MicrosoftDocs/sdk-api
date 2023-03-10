---
UID: NF:oaidl.ICreateTypeLib2.SetHelpStringContext
title: ICreateTypeLib2::SetHelpStringContext (oaidl.h)
description: Sets the Help string context number.
helpviewer_keywords: ["ICreateTypeLib2 interface [Automation]","SetHelpStringContext method","ICreateTypeLib2.SetHelpStringContext","ICreateTypeLib2::SetHelpStringContext","SetHelpStringContext","SetHelpStringContext method [Automation]","SetHelpStringContext method [Automation]","ICreateTypeLib2 interface","_oa96_ICreateTypeLib2_SetHelpStringContext","automat.icreatetypelib2_sethelpstringcontext","oaidl/ICreateTypeLib2::SetHelpStringContext"]
old-location: automat\icreatetypelib2_sethelpstringcontext.htm
tech.root: automat
ms.assetid: 35093252-74ff-4161-bf3d-f5e6b69e73c1
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib2 interface [Automation],SetHelpStringContext method, ICreateTypeLib2.SetHelpStringContext, ICreateTypeLib2::SetHelpStringContext, SetHelpStringContext, SetHelpStringContext method [Automation], SetHelpStringContext method [Automation],ICreateTypeLib2 interface, _oa96_ICreateTypeLib2_SetHelpStringContext, automat.icreatetypelib2_sethelpstringcontext, oaidl/ICreateTypeLib2::SetHelpStringContext
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
 - ICreateTypeLib2::SetHelpStringContext
 - oaidl/ICreateTypeLib2::SetHelpStringContext
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
 - ICreateTypeLib2.SetHelpStringContext
---

# ICreateTypeLib2::SetHelpStringContext


## -description

Sets the Help string context number.

## -parameters

### -param dwHelpStringContext [in]

The Help string context number.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib2">ICreateTypeLib2</a>