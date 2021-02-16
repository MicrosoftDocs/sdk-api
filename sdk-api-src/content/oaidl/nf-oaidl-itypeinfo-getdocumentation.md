---
UID: NF:oaidl.ITypeInfo.GetDocumentation
title: ITypeInfo::GetDocumentation (oaidl.h)
description: Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description.
helpviewer_keywords: ["GetDocumentation","GetDocumentation method [Automation]","GetDocumentation method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetDocumentation method","ITypeInfo.GetDocumentation","ITypeInfo::GetDocumentation","_oa96_ITypeInfo_GetDocumentation","automat.itypeinfo_getdocumentation","oaidl/ITypeInfo::GetDocumentation"]
old-location: automat\itypeinfo_getdocumentation.htm
tech.root: automat
ms.assetid: 64d2cb0c-d0ca-499b-b089-44525f7f9749
ms.date: 12/05/2018
ms.keywords: GetDocumentation, GetDocumentation method [Automation], GetDocumentation method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetDocumentation method, ITypeInfo.GetDocumentation, ITypeInfo::GetDocumentation, _oa96_ITypeInfo_GetDocumentation, automat.itypeinfo_getdocumentation, oaidl/ITypeInfo::GetDocumentation
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
 - ITypeInfo::GetDocumentation
 - oaidl/ITypeInfo::GetDocumentation
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
 - ITypeInfo.GetDocumentation
---

# ITypeInfo::GetDocumentation


## -description

Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description.

## -parameters

### -param memid [in]

The ID of the member whose documentation is to be returned.

### -param pBstrName [out]

The name of the specified item. If the caller does not need the item name, <i>pBstrName</i> can be null.

### -param pBstrDocString [out]

The documentation string for the specified item. If the caller does not need the documentation string, <i>pBstrDocString</i> can be null.

### -param pdwHelpContext [out]

The Help localization context. If the caller does not need the Help context, it can be null.

### -param pBstrHelpFile [out]

The fully qualified name of the file containing the DLL used for Help file. If the caller does not need the file name, it can be null.

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

The function <b>GetDocumentation</b> provides access to the documentation for the member specified by the <i>memid</i> parameter. If the passed-in <i>memid</i> is MEMBERID_NIL, then the documentation for the type description is returned.



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.



The caller should use <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the BSTRs referenced by <i>pBstrName</i>, <i>pBstrDocString</i>, and <i>pBstrHelpFile</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>