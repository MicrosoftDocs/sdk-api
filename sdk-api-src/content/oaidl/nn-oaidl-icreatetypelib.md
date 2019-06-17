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
f1_keywords: ["oaidl/ICreateTypeLib"]
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeLib</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateTypeLib</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-createtypeinfo">CreateTypeInfo</a>
</td>
<td align="left" width="63%">
Creates a new type description instance within the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-saveallchanges">SaveAllChanges</a>
</td>
<td align="left" width="63%">
Saves the <b>ICreateTypeLib</b> instance following the layout of type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-setdocstring">SetDocString</a>
</td>
<td align="left" width="63%">
Sets the documentation string associated with the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-setguid">SetGuid</a>
</td>
<td align="left" width="63%">
Sets the universal unique identifier (UUID) associated with the type library

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-sethelpcontext">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context ID for retrieving general Help information for the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-sethelpfilename">SetHelpFileName</a>
</td>
<td align="left" width="63%">
Sets the name of the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/lcid">SetLcid</a>
</td>
<td align="left" width="63%">
Sets the binary Microsoft national language ID associated with the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-setlibflags">SetLibFlags</a>
</td>
<td align="left" width="63%">
Sets library flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-setname">SetName</a>
</td>
<td align="left" width="63%">
Sets the name of the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib-setversion">SetVersion</a>
</td>
<td align="left" width="63%">
Sets the major and minor version numbers of the type library.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
 

 

