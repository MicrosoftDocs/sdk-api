---
UID: NN:oaidl.ICreateTypeLib2
title: ICreateTypeLib2 (oaidl.h)
author: windows-sdk-content
description: Provides the methods for creating and managing the component or file that contains type information.
old-location: automat\icreatetypelib2.htm
tech.root: automat
ms.assetid: 97378353-8c2d-493a-8ee9-42d33ab47d18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib2, ICreateTypeLib2 interface [Automation], ICreateTypeLib2 interface [Automation],described, _oa96_ICreateTypeLib2_Interface, automat.icreatetypelib2, oaidl/ICreateTypeLib2
ms.topic: interface
f1_keywords: 
 - "oaidl/ICreateTypeLib2"
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
 - ICreateTypeLib2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateTypeLib2 interface


## -description


Provides the methods for creating and managing the component or file that contains type information. Derives from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a> instance returned from <b>ICreateTypeLib</b> can be accessed through a <b>QueryInterface</b> call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeLib2</b> interface inherits from <b>ICreateTypeLib</b>. <b>ICreateTypeLib2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateTypeLib2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib2-deletetypeinfo">DeleteTypeInfo</a>
</td>
<td align="left" width="63%">
Deletes a specified type information from the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib2-setcustdata">SetCustData</a>
</td>
<td align="left" width="63%">
Sets a value to custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib2-sethelpstringcontext">SetHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets the Help string context number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypelib2-sethelpstringdll">SetHelpStringDll</a>
</td>
<td align="left" width="63%">
Sets the DLL name to be used for Help string lookup (for localization purposes).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
 

 

