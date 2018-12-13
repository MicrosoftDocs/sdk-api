---
UID: NN:oaidl.ITypeInfo2
title: ITypeInfo2
author: windows-sdk-content
description: Used for reading information about objects.
old-location: automat\itypeinfo2.htm
tech.root: automat
ms.assetid: d3a34a13-6114-4f15-9de5-60da43fde600
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITypeInfo2, ITypeInfo2 interface [Automation], ITypeInfo2 interface [Automation],described, _oa96_ITypeInfo2_Interface, automat.itypeinfo2, oaidl/ITypeInfo2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITypeInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeInfo2 interface


## -description


Used for reading information about objects. Can be cast to an <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> instead of using the calls <b>QueryInterface</b> and <b>Release</b> to allow quick opens and allocs. This only works for in-process cases.


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
<a href="https://msdn.microsoft.com/ba91134e-0d0a-4f33-a527-700f83344055">GetAllCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data items for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65ea243f-fe13-4443-80e9-4b19cf0cb8c8">GetAllFuncCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data from the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/021849d8-ec61-4f35-8302-caa8338a8758">GetAllImplTypeCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data for the specified implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb5ab67e-b5ff-40fd-a25f-d8dfb1e2c636">GetAllParamCustData</a>
</td>
<td align="left" width="63%">
Gets all of the custom data for the specified function parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d123b63e-8393-4c76-914e-87aa399aae1c">GetAllVarCustData</a>
</td>
<td align="left" width="63%">
Gets the variable for the custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c80a357-0967-413f-a211-c3bae8700b36">GetCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f81cb34-5f4e-4637-9776-e7c5353349b7">GetDocumentation2</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3a7b13f-6296-45ee-9697-4d52b5965c4b">GetFuncCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data from the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dad5fd34-9322-46aa-9ae3-d5ff9d1639b1">GetFuncIndexOfMemId</a>
</td>
<td align="left" width="63%">
Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cb30f35-8ef0-482a-bd1f-83445c97fb1f">GetImplTypeCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9342c364-58bb-47fa-b2c0-aae7df1ccdb5">GetParamCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a240caf6-f7a2-41c4-9950-f0d2df1f3e2d">GetTypeFlags</a>
</td>
<td align="left" width="63%">
Returns the type flags without any allocations. This returns a flag that expands the type flags without growing the TYPEATTR (type attribute).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ad42274-1952-44b4-ac11-93eacc10a9a9">GetTypeKind</a>
</td>
<td align="left" width="63%">
Returns the TYPEKIND enumeration quickly, without doing any allocations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe033b80-427d-48d1-99c8-4aba8909897e">GetVarCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data of the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b97ddbf-bcb3-4e39-a355-40c1fd4e8c6a">GetVarIndexOfMemId</a>
</td>
<td align="left" width="63%">
Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

</td>
</tr>
</table> 


## -see-also




<a href="387d44b7-407b-44a9-9239-a4cb20e88cac">Type Description Interfaces and Functions </a>
 

 

