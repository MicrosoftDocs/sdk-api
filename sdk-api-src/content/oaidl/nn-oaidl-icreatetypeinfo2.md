---
UID: NN:oaidl.ICreateTypeInfo2
title: ICreateTypeInfo2
author: windows-sdk-content
description: Provides the tools for creating and administering the type information defined through the type description.
old-location: automat\icreatetypeinfo2.htm
tech.root: automat
ms.assetid: 34dc6f52-6864-4edb-b22d-80eef05d4c8c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICreateTypeInfo2, ICreateTypeInfo2 interface [Automation], ICreateTypeInfo2 interface [Automation],described, _oa96_ICreateTypeInfo2_Interface, automat.icreatetypeinfo2, oaidl/ICreateTypeInfo2
ms.prod: windows
ms.technology: windows-sdk
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
---

# ICreateTypeInfo2 interface


## -description


Provides the tools for creating and administering the type information defined through the type description. Derives from <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>, and adds methods for deleting items that have been added through ICreateTypeInfo.

The <a href="https://msdn.microsoft.com/3880aad3-8a6f-43e6-8420-25c4d1b9a71a">ICreateTypeInfo::LayOut</a> method provides a way for the creator of the type information to check for any errors. A call to QueryInterface can be made to the ICreateTypeInfo instance at any time for its ITypeInfo interface. Calling any of the methods in the ITypeInfointerface that require layout information lays out the type information automatically.


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
<a href="https://msdn.microsoft.com/5e157287-e4f3-49c4-9c18-a7b3ba1a965d">DeleteFuncDesc</a>
</td>
<td align="left" width="63%">
Deletes a function description specified by the index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75de562b-3c08-4bab-957a-3a9eab16fb3f">DeleteFuncDescByMemId</a>
</td>
<td align="left" width="63%">
Deletes the specified function description (FUNCDESC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c64b70eb-6047-4572-9d5e-f40b3c302f31">DeleteImplType</a>
</td>
<td align="left" width="63%">
Deletes the IMPLTYPE flags for the indexed interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fcf55d9-2592-4fed-9612-48085eb7791b">DeleteVarDesc</a>
</td>
<td align="left" width="63%">
Deletes the specified VARDESC structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b69dda9-01b5-45b2-ab92-65a29a2d1f21">DeleteVarDescByMemId</a>
</td>
<td align="left" width="63%">
Deletes the specified VARDESC structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52a947c8-2860-4803-9df2-7b71b8b8ef87">SetCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/553e872f-0620-4b36-a01d-86088bd12f80">SetFuncCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee0fad66-632e-48f7-bd38-b17c82be555b">SetFuncHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets a Help context value for a specified function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f8ed63a-1cbb-4fd3-a848-aeb8123adf04">SetHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets the context number for the specified Help string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9dee7fc-b713-4a68-a8ea-2398a266e728">SetImplTypeCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified implementation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b490dcb5-97e4-427a-bc87-22f38a4719f3">SetName</a>
</td>
<td align="left" width="63%">
Sets the name of the typeinfo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df1a1ab0-c971-4d3e-ba63-45be66330027">SetParamCustData</a>
</td>
<td align="left" width="63%">
Sets a value for the custom data for the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7055ad6b-89d8-47d9-bdfa-26b323e53133">SetVarCustData</a>
</td>
<td align="left" width="63%">
Sets a value for custom data for the specified variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0939e286-150c-4258-bb6a-c020b6323b35">SetVarHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets a Help context value for a specified variable.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aad137b1-b747-4d74-8d6c-5ec9b6e6983d">Type Building Interfaces and Functions </a>
 

 

