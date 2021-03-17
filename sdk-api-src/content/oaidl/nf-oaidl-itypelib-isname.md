---
UID: NF:oaidl.ITypeLib.IsName
title: ITypeLib::IsName (oaidl.h)
description: Indicates whether a passed-in string contains the name of a type or member described in the library.
helpviewer_keywords: ["ITypeLib interface [Automation]","IsName method","ITypeLib.IsName","ITypeLib::IsName","IsName","IsName method [Automation]","IsName method [Automation]","ITypeLib interface","_oa96_ITypeLib_IsName","automat.itypelib_isname","oaidl/ITypeLib::IsName"]
old-location: automat\itypelib_isname.htm
tech.root: automat
ms.assetid: c9cd5cc8-f65f-43de-9dd4-c617b56ecadf
ms.date: 12/05/2018
ms.keywords: ITypeLib interface [Automation],IsName method, ITypeLib.IsName, ITypeLib::IsName, IsName, IsName method [Automation], IsName method [Automation],ITypeLib interface, _oa96_ITypeLib_IsName, automat.itypelib_isname, oaidl/ITypeLib::IsName
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
 - ITypeLib::IsName
 - oaidl/ITypeLib::IsName
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
 - ITypeLib.IsName
---

# ITypeLib::IsName


## -description

Indicates whether a passed-in string contains the name of a type or member described in the library.

## -parameters

### -param szNameBuf [in, out]

The string to test. If this method is successful, <i>szNameBuf</i> is modified to match the case (capitalization) found in the type library.

### -param lHashVal [in]

The hash value of <i>szNameBuf</i>.

### -param pfName [out]

True if <i>szNameBuf</i> was found in the type library; otherwise false.

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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>