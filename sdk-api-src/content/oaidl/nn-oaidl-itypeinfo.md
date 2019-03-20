---
UID: NN:oaidl.ITypeInfo
title: ITypeInfo (oaidl.h)
author: windows-sdk-content
description: Used for reading information about objects.
old-location: automat\itypeinfo.htm
tech.root: automat
ms.assetid: f3356463-3373-4279-bae1-953378aa2680
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITypeInfo, ITypeInfo interface [Automation], ITypeInfo interface [Automation],described, _oa96_ITypeInfo_Interface, automat.itypeinfo, oaidl/ITypeInfo
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
 - ITypeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeInfo interface


## -description


This section describes <b>ITypeInfo</b>, an interface typically used for reading information about objects. For example, an object browser tool can use <b>ITypeInfo</b> to extract information about the characteristics and capabilities of objects from type libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITypeInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cf351457-13ff-4e40-9d92-89c6db42627c">AddressOfMember</a>
</td>
<td align="left" width="63%">
Retrieves the addresses of static functions or variables, such as those defined in a DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b11c51e6-8ae7-482d-87eb-8175ca98eb63">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of a type that describes a component object class (coclass).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ca58285-4778-4c2a-b800-dcda9b62e328">GetContainingTypeLib</a>
</td>
<td align="left" width="63%">
Retrieves the containing type library and the index of the type description within that type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b947de4-4a3e-40f3-837b-c60b0ab67ef1">GetDllEntry</a>
</td>
<td align="left" width="63%">
Retrieves a description or specification of an entry point for a function in a DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64d2cb0c-d0ca-499b-b089-44525f7f9749">GetDocumentation</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e3331a2-0156-4d8f-aa7f-e32cecd3eb74">GetFuncDesc</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/9998e0cb-5aa3-4cd8-86eb-34760eb1164e">FUNCDESC</a> structure that contains information about a specified function

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb66ee55-e491-40e9-a795-58beb4acee25">GetIDsOfNames</a>
</td>
<td align="left" width="63%">
Maps between member names and member IDs, and parameter names and parameter IDs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3773111-b09d-4ae0-9a91-3c4adff5b803">GetImplTypeFlags</a>
</td>
<td align="left" width="63%">
Retrieves the IMPLTYPEFLAGS enumeration for one implemented interface or base interface in a type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f8f4d4a-c51d-46d3-ad0f-1ee357bb7104">GetMops</a>
</td>
<td align="left" width="63%">
Retrieves marshaling information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff318d92-9624-48aa-a0f9-8b8826121753">GetNames</a>
</td>
<td align="left" width="63%">
Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">GetRefTypeInfo</a>
</td>
<td align="left" width="63%">
If a type description references other type descriptions, it retrieves the referenced type descriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aec61a9a-fa4f-42cd-a74b-100cdf2c2624">GetRefTypeOfImplType</a>
</td>
<td align="left" width="63%">
If a type description describes a COM class, it retrieves the type description of the implemented interface types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62be8a38-1d51-4b54-b224-7d9cdbb1be59">GetTypeAttr</a>
</td>
<td align="left" width="63%">
Retrieves a TYPEATTR structure that contains the attributes of the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/094cf9d5-2d9b-4c3c-844e-45737e905099">GetTypeComp</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> interface for the type description, which enables a client compiler to bind to the type description's members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4226d33-37ec-4e9a-87ce-92c4ff0e6cb3">GetVarDesc</a>
</td>
<td align="left" width="63%">
Retrieves a VARDESC structure that describes the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dde2ca58-84bd-4a49-a160-a9955d691f3b">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a method, or accesses a property of an object, that implements the interface described by the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c407301-87fd-4f79-89e1-c6db5d1cf36b">ReleaseFuncDesc</a>
</td>
<td align="left" width="63%">
Releases a FUNCDESC previously returned by <a href="https://msdn.microsoft.com/1e3331a2-0156-4d8f-aa7f-e32cecd3eb74">ITypeInfo::GetFuncDesc</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86827f7f-d5c7-4297-8eb9-af7b03d16121">ReleaseTypeAttr</a>
</td>
<td align="left" width="63%">
Releases a TYPEATTR previously returned by <a href="https://msdn.microsoft.com/62be8a38-1d51-4b54-b224-7d9cdbb1be59">ITypeInfo::GetTypeAttr</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0f734d8-9b14-474a-b701-df8ba7641501">ReleaseVarDesc</a>
</td>
<td align="left" width="63%">
Releases a VARDESC previously returned by <a href="https://msdn.microsoft.com/c4226d33-37ec-4e9a-87ce-92c4ff0e6cb3">ITypeInfo::GetVarDesc</a>.

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
The type description of an <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface can be used to implement the interface. For more information, see the description of <a href="https://msdn.microsoft.com/en-us/library/ms221135(v=VS.85).aspx">CreateStdDispatch</a> in <a href="https://msdn.microsoft.com/en-us/library/ms221328(v=VS.85).aspx">Dispatch Interface and API Functions</a>. 

An instance of <b>ITypeInfo</b> provides various information about the type of an object, and is used in different ways. A compiler can use an <b>ITypeInfo</b> to compile references to members of the type. A type interface browser can use it to find information about each member of the type. An <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> implementor can use it to provide automatic delegation of <b>IDispatch</b> calls to an interface.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221172(v=VS.85).aspx">Type Description Interfaces and Functions </a>
 

 

