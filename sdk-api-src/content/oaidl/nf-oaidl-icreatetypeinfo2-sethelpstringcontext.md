---
UID: NF:oaidl.ICreateTypeInfo2.SetHelpStringContext
title: ICreateTypeInfo2::SetHelpStringContext (oaidl.h)
description: Sets the context number for the specified Help string.
helpviewer_keywords: ["ICreateTypeInfo2 interface [Automation]","SetHelpStringContext method","ICreateTypeInfo2.SetHelpStringContext","ICreateTypeInfo2::SetHelpStringContext","SetHelpStringContext","SetHelpStringContext method [Automation]","SetHelpStringContext method [Automation]","ICreateTypeInfo2 interface","_oa96_ICreateTypeInfo2_SetHelpStringContext","automat.icreatetypeinfo2_sethelpstringcontext","oaidl/ICreateTypeInfo2::SetHelpStringContext"]
old-location: automat\icreatetypeinfo2_sethelpstringcontext.htm
tech.root: automat
ms.assetid: 2f8ed63a-1cbb-4fd3-a848-aeb8123adf04
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetHelpStringContext method, ICreateTypeInfo2.SetHelpStringContext, ICreateTypeInfo2::SetHelpStringContext, SetHelpStringContext, SetHelpStringContext method [Automation], SetHelpStringContext method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetHelpStringContext, automat.icreatetypeinfo2_sethelpstringcontext, oaidl/ICreateTypeInfo2::SetHelpStringContext
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
 - ICreateTypeInfo2::SetHelpStringContext
 - oaidl/ICreateTypeInfo2::SetHelpStringContext
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
 - ICreateTypeInfo2.SetHelpStringContext
---

# ICreateTypeInfo2::SetHelpStringContext


## -description

Sets the context number for the specified Help string.

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