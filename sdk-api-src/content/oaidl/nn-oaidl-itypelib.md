---
UID: NN:oaidl.ITypeLib
title: ITypeLib (oaidl.h)
author: windows-sdk-content
description: Represents a type library, the data that describes a set of objects.
old-location: automat\itypelib.htm
tech.root: automat
ms.assetid: c1e5d71f-6a4e-45f3-811d-f57024f81a55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITypeLib, ITypeLib interface [Automation], ITypeLib interface [Automation],described, _oa96_ITypeLib_Interface, automat.itypelib, oaidl/ITypeLib
ms.topic: interface
f1_keywords: 
 - "oaidl/ITypeLib"
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
 - ITypeLib
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITypeLib interface


## -description


Represents a type library, the data that describes a set of objects. A type library can be a stand-alone binary file (.TLB), a resource in a dynamic link library or executable file (.DLL, .OLB, or .EXE).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeLib</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeLib</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-findname">FindName</a>
</td>
<td align="left" width="63%">
Finds occurrences of a type description in a type library. This may be used to quickly verify that a name exists in a type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-getdocumentation">GetDocumentation</a>
</td>
<td align="left" width="63%">
Retrieves the documentation string for the library, the complete Help file name and path, and the context identifier for the library Help topic in the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-getlibattr">GetLibAttr</a>
</td>
<td align="left" width="63%">
Retrieves the structure that contains the library's attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypecomp">GetTypeComp</a>
</td>
<td align="left" width="63%">
Enables a client compiler to bind to the types, variables, constants, and global functions for a library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfo">GetTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the specified type description in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfocount">GetTypeInfoCount</a>
</td>
<td align="left" width="63%">
Provides the number of type descriptions that are in a type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfoofguid">GetTypeInfoOfGuid</a>
</td>
<td align="left" width="63%">
Retrieves the type description that corresponds to the specified GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfotype">GetTypeInfoType</a>
</td>
<td align="left" width="63%">
Retrieves the type of a type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-isname">IsName</a>
</td>
<td align="left" width="63%">
Indicates whether a passed-in string contains the name of a type or member described in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-releasetlibattr">ReleaseTLibAttr</a>
</td>
<td align="left" width="63%">
Releases the TLIBATTR originally obtained from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-getlibattr">GetLibAttr</a>.

</td>
</tr>
</table> 


## -remarks



The system registry contains a list of all the installed type libraries. Type library organization is illustrated in the following figure:

<img alt="" src="./images/oa03_10.Png"/>
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




<a href="https://docs.microsoft.com/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>
 

 

