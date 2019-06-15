---
UID: NN:oaidl.ICreateTypeInfo2
title: ICreateTypeInfo2 (oaidl.h)
author: windows-sdk-content
description: Provides the tools for creating and administering the type information defined through the type description.
old-location: automat\icreatetypeinfo2.htm
tech.root: automat
ms.assetid: 34dc6f52-6864-4edb-b22d-80eef05d4c8c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2, ICreateTypeInfo2 interface [Automation], ICreateTypeInfo2 interface [Automation],described, _oa96_ICreateTypeInfo2_Interface, automat.icreatetypeinfo2, oaidl/ICreateTypeInfo2
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateTypeInfo2 interface


## -description


Provides the tools for creating and administering the type information defined through the type description. Derives from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>, and adds methods for deleting items that have been added through ICreateTypeInfo.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/out">ICreateTypeInfo::LayOut</a> method provides a way for the creator of the type information to check for any errors. A call to QueryInterface can be made to the ICreateTypeInfo instance at any time for its ITypeInfo interface. Calling any of the methods in the ITypeInfointerface that require layout information lays out the type information automatically.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeInfo2</b> interface inherits from <b>ICreateTypeInfo</b>. <b>ICreateTypeInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateTypeInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-deletefuncdesc">DeleteFuncDesc</a>
</td>
<td align="left" width="63%">
Deletes a function description specified by the index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-deletefuncdescbymemid">DeleteFuncDescByMemId</a>
</td>
<td align="left" width="63%">
Deletes the specified function description (FUNCDESC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-deleteimpltype">DeleteImplType</a>
</td>
<td align="left" width="63%">
Deletes the IMPLTYPE flags for the indexed interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-deletevardesc">DeleteVarDesc</a>
</td>
<td align="left" width="63%">
Deletes the specified VARDESC structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-deletevardescbymemid">DeleteVarDescByMemId</a>
</td>
<td align="left" width="63%">
Deletes the specified VARDESC structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setcustdata">SetCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setfunccustdata">SetFuncCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setfunchelpstringcontext">SetFuncHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets a Help context value for a specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-sethelpstringcontext">SetHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets the context number for the specified Help string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setimpltypecustdata">SetImplTypeCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setname">SetName</a>
</td>
<td align="left" width="63%">
Sets the name of the typeinfo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setparamcustdata">SetParamCustData</a>
</td>
<td align="left" width="63%">
Sets a value for the custom data for the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setvarcustdata">SetVarCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo2-setvarhelpstringcontext">SetVarHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets a Help context value for a specified variable.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
 

 

