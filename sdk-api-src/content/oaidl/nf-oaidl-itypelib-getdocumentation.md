---
UID: NF:oaidl.ITypeLib.GetDocumentation
title: ITypeLib::GetDocumentation (oaidl.h)
description: Retrieves the documentation string for the library, the complete Help file name and path, and the context identifier for the library Help topic in the Help file.
helpviewer_keywords: ["GetDocumentation","GetDocumentation method [Automation]","GetDocumentation method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","GetDocumentation method","ITypeLib.GetDocumentation","ITypeLib::GetDocumentation","_oa96_ITypeLib_GetDocumentation","automat.itypelib_getdocumentation","oaidl/ITypeLib::GetDocumentation"]
old-location: automat\itypelib_getdocumentation.htm
tech.root: automat
ms.assetid: aa65e143-47db-4241-9c66-fe3a1dcf1f0a
ms.date: 12/05/2018
ms.keywords: GetDocumentation, GetDocumentation method [Automation], GetDocumentation method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetDocumentation method, ITypeLib.GetDocumentation, ITypeLib::GetDocumentation, _oa96_ITypeLib_GetDocumentation, automat.itypelib_getdocumentation, oaidl/ITypeLib::GetDocumentation
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
 - ITypeLib::GetDocumentation
 - oaidl/ITypeLib::GetDocumentation
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
 - ITypeLib.GetDocumentation
---

# ITypeLib::GetDocumentation


## -description

Retrieves the documentation string for the library, the complete Help file name and path, and the context identifier for the library Help topic in the Help file.

## -parameters

### -param index [in]

The index of the type description whose documentation is to be returned. If <i>index</i> is -1, then the documentation for the library itself is returned.

### -param pBstrName [out]

The name of the specified item. If the caller does not need the item name, then <i>pBstrName</i> can be null.

### -param pBstrDocString [out]

The documentation string for the specified item. If the caller does not need the documentation string, then <i>pBstrDocString</i> can be null..

### -param pdwHelpContext [out]

The Help context identifier (ID) associated with the specified item. If the caller does not need the Help context ID, then <i>pdwHelpContext</i> can be null.

### -param pBstrHelpFile [out]

 The fully qualified name of the Help file. If the caller does not need the Help file name, then <i>pBstrHelpFile</i> can be null.

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
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The caller should free the parameters <i>pBstrName</i>, <i>pBstrDocString</i>, and <i>pBstrHelpFile</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>