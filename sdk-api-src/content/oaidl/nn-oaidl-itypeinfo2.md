---
UID: NN:oaidl.ITypeInfo2
title: ITypeInfo2 (oaidl.h)
description: Used for reading information about objects.
helpviewer_keywords: ["ITypeInfo2","ITypeInfo2 interface [Automation]","ITypeInfo2 interface [Automation]","described","_oa96_ITypeInfo2_Interface","automat.itypeinfo2","oaidl/ITypeInfo2"]
old-location: automat\itypeinfo2.htm
tech.root: automat
ms.assetid: d3a34a13-6114-4f15-9de5-60da43fde600
ms.date: 12/05/2018
ms.keywords: ITypeInfo2, ITypeInfo2 interface [Automation], ITypeInfo2 interface [Automation],described, _oa96_ITypeInfo2_Interface, automat.itypeinfo2, oaidl/ITypeInfo2
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
 - ITypeInfo2
 - oaidl/ITypeInfo2
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
 - ITypeInfo2
---

# ITypeInfo2 interface


## -description

Used for reading information about objects. Can be cast to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> instead of using the calls <b>QueryInterface</b> and <b>Release</b> to allow quick opens and allocs. This only works for in-process cases.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeInfo2</b> interface inherits from <b>ITypeInfo</b>. <b>ITypeInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getallcustdata">GetAllCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data items for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getallfunccustdata">GetAllFuncCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data from the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getallimpltypecustdata">GetAllImplTypeCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data for the specified implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getallparamcustdata">GetAllParamCustData</a>
</td>
<td align="left" width="63%">
Gets all of the custom data for the specified function parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getallvarcustdata">GetAllVarCustData</a>
</td>
<td align="left" width="63%">
Gets the variable for the custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getcustdata">GetCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getdocumentation2">GetDocumentation2</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getfunccustdata">GetFuncCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data from the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getfuncindexofmemid">GetFuncIndexOfMemId</a>
</td>
<td align="left" width="63%">
Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getimpltypecustdata">GetImplTypeCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getparamcustdata">GetParamCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-gettypeflags">GetTypeFlags</a>
</td>
<td align="left" width="63%">
Returns the type flags without any allocations. This returns a flag that expands the type flags without growing the TYPEATTR (type attribute).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-gettypekind">GetTypeKind</a>
</td>
<td align="left" width="63%">
Returns the TYPEKIND enumeration quickly, without doing any allocations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getvarcustdata">GetVarCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo2-getvarindexofmemid">GetVarIndexOfMemId</a>
</td>
<td align="left" width="63%">
Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>