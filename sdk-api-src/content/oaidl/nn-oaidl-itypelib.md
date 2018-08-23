---
UID: NN:oaidl.ITypeLib
title: ITypeLib
author: windows-sdk-content
description: Represents a type library, the data that describes a set of objects.
old-location: automat\itypelib.htm
old-project: automat
ms.assetid: c1e5d71f-6a4e-45f3-811d-f57024f81a55
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITypeLib, ITypeLib interface [Automation], ITypeLib interface [Automation],described, _oa96_ITypeLib_Interface, automat.itypelib, oaidl/ITypeLib
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeLib
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# ITypeLib interface


## -description


Represents a type library, the data that describes a set of objects. A type library can be a stand-alone binary file (.TLB), a resource in a dynamic link library or executable file (.DLL, .OLB, or .EXE).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeLib</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITypeLib</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeLib</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/932014a8-3a35-487a-b035-788fc28dacc2">FindName</a>
</td>
<td align="left" width="63%">
Finds occurrences of a type description in a type library. This may be used to quickly verify that a name exists in a type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa65e143-47db-4241-9c66-fe3a1dcf1f0a">GetDocumentation</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string for the library, the complete Help file name and path, and the context identifier for the library Help topic in the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edc35364-99dc-438b-81de-4f129c0cf50f">GetLibAttr</a>
</td>
<td align="left" width="63%">
Retrieves the structure that contains the library's attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11c22e52-b0d5-4251-b8fa-ea3efae555e6">GetTypeComp</a>
</td>
<td align="left" width="63%">
Enables a client compiler to bind to the types, variables, constants, and global functions for a library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7661faa8-eb06-4bbe-88e9-9662a0d6984b">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the specified type description in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63436bee-c71b-4d32-bfca-426c8953a75b">GetTypeInfoCount</a>
</td>
<td align="left" width="63%">
Provides the number of type descriptions that are in a type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58f96322-f1cd-448c-906d-b7faa65ab9a0">GetTypeInfoOfGuid</a>
</td>
<td align="left" width="63%">
Retrieves the type description that corresponds to the specified GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e0924ee-41f1-4f0a-a491-40b92bd0711e">GetTypeInfoType</a>
</td>
<td align="left" width="63%">
Retrieves the type of a type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9cd5cc8-f65f-43de-9dd4-c617b56ecadf">IsName</a>
</td>
<td align="left" width="63%">
Indicates whether a passed-in string contains the name of a type or member described in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5b9ee66-ab66-4ad9-a6bf-93bd98e3905c">ReleaseTLibAttr</a>
</td>
<td align="left" width="63%">
Releases the TLIBATTR originally obtained from <a href="https://msdn.microsoft.com/edc35364-99dc-438b-81de-4f129c0cf50f">GetLibAttr</a>.

</td>
</tr>
</table> 


## -remarks



The system registry contains a list of all the installed type libraries. Type library organization is illustrated in the following figure:

<img alt="" src="images/oa03_10.Png"/>
The <b>ITypeLib</b> interface provides methods for accessing a library of type descriptions. This interface supports the following:  

<ul>
<li>
Generalized containment for type information. <b>ITypeLib</b> allows iteration over the type descriptions contained in the library.

</li>
<li>
Global functions and data. A type library can contain descriptions of a set of modules (.DLLs) that exports data and functions. The type library supports compiling references to the exported data and functions.

</li>
<li>
General information, including a user-readable name for the library and help for the library as a whole.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/ms221172(v=VS.85).aspx">Type Description Interfaces and Functions </a>
 

 

