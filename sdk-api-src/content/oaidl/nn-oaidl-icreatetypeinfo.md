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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateTypeInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f6816778-86f6-4e59-8eb2-444fd7bd6354">AddFuncDesc</a>
</td>
<td align="left" width="63%">
Adds a function description to the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fef8421f-67de-402b-8efd-7a104c84ca6e">AddImplType</a>
</td>
<td align="left" width="63%">
Specifies an inherited interface, or an interface implemented by a component object class (coclass).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb7f41f1-81a6-406f-916f-d1d1a8c093b5">AddRefTypeInfo</a>
</td>
<td align="left" width="63%">
Adds a type description to those referenced by the type description being created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db576528-fefc-4a22-bc24-d5ea037eae26">AddVarDesc</a>
</td>
<td align="left" width="63%">
Adds a variable or data member description to the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ec09af-0642-4645-b946-acabbb7c028a">DefineFuncAsDllEntry</a>
</td>
<td align="left" width="63%">
Associates a DLL entry point with the function that has the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3880aad3-8a6f-43e6-8420-25c4d1b9a71a">LayOut</a>
</td>
<td align="left" width="63%">
Assigns VTBL offsets for virtual functions and instance offsets for per-instance data members, and creates the two type descriptions for dual interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db21ab80-ea2f-4f9e-a43c-0d202e235516">SetAlignment</a>
</td>
<td align="left" width="63%">
Specifies the data alignment for an item of TYPEKIND=TKIND_RECORD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/927c449b-1d38-4449-a1fd-63fb82c0d660">SetDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string displayed by type browsers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3764917-43ea-4151-95da-e01946a2ebb7">SetFuncAndParamNames</a>
</td>
<td align="left" width="63%">
Sets the name of a function and the names of its parameters to the specified names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2377502-b26f-401f-82f1-d65f739a684f">SetFuncDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string for the function with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/945d2faa-f35d-488f-a0df-ace3fbb85971">SetFuncHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for the function with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/031bc83d-8e0c-49da-aa15-cd44af469592">SetGuid</a>
</td>
<td align="left" width="63%">
Sets the globally unique identifier (GUID) associated with the type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f61500a-29b5-48e4-b8ee-584cf5430274">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID of the type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/712b7d02-0181-4a21-9221-514c062af171">SetImplTypeFlags</a>
</td>
<td align="left" width="63%">
Sets the attributes for an implemented or inherited interface of a type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e775c2f9-2886-4aa0-a30c-445f317d0e02">SetMops</a>
</td>
<td align="left" width="63%">
Sets the marshaling opcode string associated with the type description or the function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63435592-9fc8-4d49-a388-87f1d15f2603">SetTypeDescAlias</a>
</td>
<td align="left" width="63%">
Sets the type description for which this type description is an alias, if TYPEKIND=TKIND_ALIAS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dfc1673-6242-4beb-978f-85f2000fab8e">SetTypeFlags</a>
</td>
<td align="left" width="63%">
Sets type flags of the type description being created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bea2b52-30d8-454c-ad96-f94417640ce5">SetVarDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string for the variable with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab15e7fc-63fa-433f-9191-c7087143a7c1">SetVarHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for the variable with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f51fc2a-74cc-4aab-89b7-0237c14ff7f5">SetVarName</a>
</td>
<td align="left" width="63%">
Sets the name of a variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffa4d287-44c4-40ec-984a-70cbc0928274">SetVersion</a>
</td>
<td align="left" width="63%">
Sets the major and minor version number of the type information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aad137b1-b747-4d74-8d6c-5ec9b6e6983d">Type Building Interfaces and Functions </a>
 

 

