---
UID: NN:oaidl.ICreateTypeInfo
title: ICreateTypeInfo (oaidl.h)
author: windows-sdk-content
description: Provides the tools for creating and administering the type information defined through the type description.
old-location: automat\icreatetypeinfo.htm
tech.root: automat
ms.assetid: c8bbb677-2666-4900-8fb9-788742eef656
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo, ICreateTypeInfo interface [Automation], ICreateTypeInfo interface [Automation],described, _oa96_ICreateTypeInfo_Interface, automat.icreatetypeinfo, oaidl/ICreateTypeInfo
ms.topic: interface
f1_keywords: ["oaidl/ICreateTypeInfo"]
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
 - ICreateTypeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateTypeInfo interface


## -description


Provides the tools for creating and administering the type information defined through the type description.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateTypeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateTypeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addfuncdesc">AddFuncDesc</a>
</td>
<td align="left" width="63%">
Adds a function description to the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addimpltype">AddImplType</a>
</td>
<td align="left" width="63%">
Specifies an inherited interface, or an interface implemented by a component object class (coclass).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addreftypeinfo">AddRefTypeInfo</a>
</td>
<td align="left" width="63%">
Adds a type description to those referenced by the type description being created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addvardesc">AddVarDesc</a>
</td>
<td align="left" width="63%">
Adds a variable or data member description to the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-definefuncasdllentry">DefineFuncAsDllEntry</a>
</td>
<td align="left" width="63%">
Associates a DLL entry point with the function that has the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/out">LayOut</a>
</td>
<td align="left" width="63%">
Assigns VTBL offsets for virtual functions and instance offsets for per-instance data members, and creates the two type descriptions for dual interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setalignment">SetAlignment</a>
</td>
<td align="left" width="63%">
Specifies the data alignment for an item of TYPEKIND=TKIND_RECORD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/string">SetDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string displayed by type browsers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setfuncandparamnames">SetFuncAndParamNames</a>
</td>
<td align="left" width="63%">
Sets the name of a function and the names of its parameters to the specified names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setfuncdocstring">SetFuncDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string for the function with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setfunchelpcontext">SetFuncHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for the function with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setguid">SetGuid</a>
</td>
<td align="left" width="63%">
Sets the globally unique identifier (GUID) associated with the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-sethelpcontext">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID of the type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/impltypeflags">SetImplTypeFlags</a>
</td>
<td align="left" width="63%">
Sets the attributes for an implemented or inherited interface of a type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setmops">SetMops</a>
</td>
<td align="left" width="63%">
Sets the marshaling opcode string associated with the type description or the function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-settypedescalias">SetTypeDescAlias</a>
</td>
<td align="left" width="63%">
Sets the type description for which this type description is an alias, if TYPEKIND=TKIND_ALIAS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-settypeflags">SetTypeFlags</a>
</td>
<td align="left" width="63%">
Sets type flags of the type description being created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setvardocstring">SetVarDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string for the variable with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setvarhelpcontext">SetVarHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for the variable with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setvarname">SetVarName</a>
</td>
<td align="left" width="63%">
Sets the name of a variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-setversion">SetVersion</a>
</td>
<td align="left" width="63%">
Sets the major and minor version number of the type information.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
 

 

