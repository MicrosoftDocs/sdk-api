---
UID: NN:oaidl.ITypeLib2
title: ITypeLib2
author: windows-sdk-content
description: Represents a type library, the data that describes a set of objects.
old-location: automat\itypelib2.htm
tech.root: automat
ms.assetid: 47561b53-3f7b-4939-8b86-5acb5eaeea5a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITypeLib2, ITypeLib2 interface [Automation], ITypeLib2 interface [Automation],described, _oa96_ITypeLib2_Interface, automat.itypelib2, oaidl/ITypeLib2
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
 - ITypeLib2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeLib2 interface


## -description


Represents a type library, the data that describes a set of objects.

The <b>ITypeLib2</b> interface inherits from the <a href="https://msdn.microsoft.com/c1e5d71f-6a4e-45f3-811d-f57024f81a55">ITypeLib</a>interface. This allows <b>ITypeLib</b> to cast to an <b>ITypeLib2</b> in performance-sensitive cases, rather than perform extra QueryInterface and Release calls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeLib2</b> interface inherits from <b>ITypeLib</b>. <b>ITypeLib2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeLib2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f557bfe6-5254-43c6-a42b-bc2d13126705">GetAllCustData</a>
</td>
<td align="left" width="63%">
Gets all custom data items for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2f29070-6768-4734-a3e2-c9258375b33c">GetCustData</a>
</td>
<td align="left" width="63%">
Gets the custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/976e3258-5dba-4d0c-916d-75449f869363">GetDocumentation2</a>
</td>
<td align="left" width="63%">
Retrieves the library's documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6ee47f7-eca6-48f6-b984-ff8c83a4ca46">GetLibStatistics</a>
</td>
<td align="left" width="63%">
Returns statistics about a type library that are required for efficient sizing of hash tables.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221172(v=VS.85).aspx">Type Description Interfaces and Functions </a>
 

 

