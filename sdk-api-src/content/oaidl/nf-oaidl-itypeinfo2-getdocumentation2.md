---
UID: NF:oaidl.ITypeInfo2.GetDocumentation2
title: ITypeInfo2::GetDocumentation2 (oaidl.h)
description: Retrieves the documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file.
helpviewer_keywords: ["GetDocumentation2","GetDocumentation2 method [Automation]","GetDocumentation2 method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetDocumentation2 method","ITypeInfo2.GetDocumentation2","ITypeInfo2::GetDocumentation2","_oa96_ITypeInfo2_GetDocumentation2","automat.itypeinfo2_getdocumentation2","oaidl/ITypeInfo2::GetDocumentation2"]
old-location: automat\itypeinfo2_getdocumentation2.htm
tech.root: automat
ms.assetid: 9f81cb34-5f4e-4637-9776-e7c5353349b7
ms.date: 12/05/2018
ms.keywords: GetDocumentation2, GetDocumentation2 method [Automation], GetDocumentation2 method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetDocumentation2 method, ITypeInfo2.GetDocumentation2, ITypeInfo2::GetDocumentation2, _oa96_ITypeInfo2_GetDocumentation2, automat.itypeinfo2_getdocumentation2, oaidl/ITypeInfo2::GetDocumentation2
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
 - ITypeInfo2::GetDocumentation2
 - oaidl/ITypeInfo2::GetDocumentation2
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
 - ITypeInfo2.GetDocumentation2
---

# ITypeInfo2::GetDocumentation2


## -description

Retrieves the documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file.

## -parameters

### -param memid [in]

The member identifier for the type description.

### -param lcid [in]

The locale identifier.

### -param pbstrHelpString [out]

The name of the specified item. If the caller does not need the item name, then <i>pbstrHelpString</i> can be null.

### -param pdwHelpStringContext [out]

The Help localization context. If the caller does not need the Help context, it can be null.

### -param pbstrHelpStringDll [out]

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

Gets information at the type information level (about the type information and its members). The caller should free the BSTR parameters.

This function will call <b>_DLLGetDocumentation</b> in the specified DLL to retrieve the desired Help string, if there is a Help string context for this item. If no Help string context exists or an error occurs, then it will defer to the <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getdocumentation">GetDocumentation</a> method and return the associated documentation string.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>