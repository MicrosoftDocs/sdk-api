---
UID: NN:oaidl.ITypeInfo
title: ITypeInfo (oaidl.h)
description: Used for reading information about objects.
helpviewer_keywords: ["ITypeInfo","ITypeInfo interface [Automation]","ITypeInfo interface [Automation]","described","_oa96_ITypeInfo_Interface","automat.itypeinfo","oaidl/ITypeInfo"]
old-location: automat\itypeinfo.htm
tech.root: automat
ms.assetid: f3356463-3373-4279-bae1-953378aa2680
ms.date: 12/05/2018
ms.keywords: ITypeInfo, ITypeInfo interface [Automation], ITypeInfo interface [Automation],described, _oa96_ITypeInfo_Interface, automat.itypeinfo, oaidl/ITypeInfo
f1_keywords:
- oaidl/ITypeInfo
dev_langs:
- c++
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
- ITypeInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITypeInfo interface


## -description


This section describes <b>ITypeInfo</b>, an interface typically used for reading information about objects. For example, an object browser tool can use <b>ITypeInfo</b> to extract information about the characteristics and capabilities of objects from type libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-addressofmember">AddressOfMember</a>
</td>
<td align="left" width="63%">
Retrieves the addresses of static functions or variables, such as those defined in a DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of a type that describes a component object class (coclass).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getcontainingtypelib">GetContainingTypeLib</a>
</td>
<td align="left" width="63%">
Retrieves the containing type library and the index of the type description within that type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getdllentry">GetDllEntry</a>
</td>
<td align="left" width="63%">
Retrieves a description or specification of an entry point for a function in a DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getdocumentation">GetDocumentation</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getfuncdesc">GetFuncDesc</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-funcdesc">FUNCDESC</a> structure that contains information about a specified function

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getidsofnames">GetIDsOfNames</a>
</td>
<td align="left" width="63%">
Maps between member names and member IDs, and parameter names and parameter IDs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getimpltypeflags">GetImplTypeFlags</a>
</td>
<td align="left" width="63%">
Retrieves the IMPLTYPEFLAGS enumeration for one implemented interface or base interface in a type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getmops">GetMops</a>
</td>
<td align="left" width="63%">
Retrieves marshaling information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getnames">GetNames</a>
</td>
<td align="left" width="63%">
Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getreftypeinfo">GetRefTypeInfo</a>
</td>
<td align="left" width="63%">
If a type description references other type descriptions, it retrieves the referenced type descriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getreftypeofimpltype">GetRefTypeOfImplType</a>
</td>
<td align="left" width="63%">
If a type description describes a COM class, it retrieves the type description of the implemented interface types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-gettypeattr">GetTypeAttr</a>
</td>
<td align="left" width="63%">
Retrieves a TYPEATTR structure that contains the attributes of the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-gettypecomp">GetTypeComp</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> interface for the type description, which enables a client compiler to bind to the type description's members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getvardesc">GetVarDesc</a>
</td>
<td align="left" width="63%">
Retrieves a VARDESC structure that describes the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a method, or accesses a property of an object, that implements the interface described by the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasefuncdesc">ReleaseFuncDesc</a>
</td>
<td align="left" width="63%">
Releases a FUNCDESC previously returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getfuncdesc">ITypeInfo::GetFuncDesc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasetypeattr">ReleaseTypeAttr</a>
</td>
<td align="left" width="63%">
Releases a TYPEATTR previously returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-gettypeattr">ITypeInfo::GetTypeAttr</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasevardesc">ReleaseVarDesc</a>
</td>
<td align="left" width="63%">
Releases a VARDESC previously returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getvardesc">ITypeInfo::GetVarDesc</a>.

</td>
</tr>
</table> 


## -remarks



Type information interfaces are intended to describe the parts of the application that can be called by outside clients, rather than those that might be used internally to build an application.

The <b>ITypeInfo</b> interface provides access to the following:  

<ul>
<li>
The set of function descriptions associated with the type. For interfaces, this contains the set of member functions in the interface.

</li>
<li>
The set of data member descriptions associated with the type. For structures, this contains the set of fields of the type.

</li>
<li>
The general attributes of the type, such as whether it describes a structure, an interface, and so on.

</li>
</ul>
The type description of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface can be used to implement the interface. For more information, see the description of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createstddispatch">CreateStdDispatch</a> in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/dispatch-interfaces">Dispatch Interface and API Functions</a>. 

An instance of <b>ITypeInfo</b> provides various information about the type of an object, and is used in different ways. A compiler can use an <b>ITypeInfo</b> to compile references to members of the type. A type interface browser can use it to find information about each member of the type. An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> implementor can use it to provide automatic delegation of <b>IDispatch</b> calls to an interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>
 

 

