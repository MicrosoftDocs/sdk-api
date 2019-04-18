---
UID: NN:oaidl.ICreateTypeLib
title: ICreateTypeLib (oaidl.h)
author: windows-sdk-content
description: Provides the methods for creating and managing the component or file that contains type information.
old-location: automat\icreatetypelib.htm
tech.root: automat
ms.assetid: d245cd25-ce31-42da-a42d-dc412d5b98e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib, ICreateTypeLib interface [Automation], ICreateTypeLib interface [Automation],described, _oa96_ICreateTypeLib_Interface, automat.icreatetypelib, oaidl/ICreateTypeLib
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
 - ICreateTypeLib
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateTypeLib interface


## -description


Provides the methods for creating and managing the component or file that contains type information. Type libraries are created from type descriptions using the MIDL compiler. These type libraries are accessed through the ITypeLib interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeLib</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateTypeLib</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateTypeLib</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e9678af-661b-4033-bd3f-607c064f4245">CreateTypeInfo</a>
</td>
<td align="left" width="63%">
Creates a new type description instance within the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67824f38-e515-487e-8f4b-6682a5ac669c">SaveAllChanges</a>
</td>
<td align="left" width="63%">
Saves the <b>ICreateTypeLib</b> instance following the layout of type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe93ad2-f3c2-4559-a64a-cbbc17448e05">SetDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string associated with the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9afbb9e-3f0a-4862-abb6-82631bae759f">SetGuid</a>
</td>
<td align="left" width="63%">
Sets the universal unique identifier (UUID) associated with the type library

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58d7cd77-cfb6-493e-a9fd-26f469eec9f0">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for retrieving general Help information for the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9dc11b0-1483-4272-84cb-4f885f6cff6f">SetHelpFileName</a>
</td>
<td align="left" width="63%">
Sets the name of the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4281058b-a617-4504-bc36-b18763b40897">SetLcid</a>
</td>
<td align="left" width="63%">
Sets the binary Microsoft national language ID associated with the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc72635c-853f-4a0a-9869-263e4aa39b8b">SetLibFlags</a>
</td>
<td align="left" width="63%">
Sets library flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b533d2a1-f008-4345-8545-aebe14aa44f5">SetName</a>
</td>
<td align="left" width="63%">
Sets the name of the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c71bf8f-998a-4a9a-a4a8-981f51334cbe">SetVersion</a>
</td>
<td align="left" width="63%">
Sets the major and minor version numbers of the type library.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aad137b1-b747-4d74-8d6c-5ec9b6e6983d">Type Building Interfaces and Functions </a>
 

 

