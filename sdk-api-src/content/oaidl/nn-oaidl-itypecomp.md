---
UID: NN:oaidl.ITypeComp
title: ITypeComp (oaidl.h)
description: The ITypeComp interface provides a fast way to access information that compilers need when binding to and instantiating structures and interfaces.
helpviewer_keywords: ["ITypeComp","ITypeComp interface [Automation]","ITypeComp interface [Automation]","described","_oa96_ITypeComp_Interface","automat.itypecomp","oaidl/ITypeComp"]
old-location: automat\itypecomp.htm
tech.root: automat
ms.assetid: 4d35370f-506f-45cd-9d75-e48c640d8f4d
ms.date: 12/05/2018
ms.keywords: ITypeComp, ITypeComp interface [Automation], ITypeComp interface [Automation],described, _oa96_ITypeComp_Interface, automat.itypecomp, oaidl/ITypeComp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITypeComp
 - oaidl/ITypeComp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeComp
---

# ITypeComp interface


## -description

The <b>ITypeComp</b> interface provides a fast way to access information that compilers need when binding to and instantiating structures and interfaces. Binding is the process of mapping names to types and type members.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeComp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeComp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeComp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bind">Bind</a>
</td>
<td align="left" width="63%">
Maps a name to a member of a type, or binds global variables and functions contained in a type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bindtype">BindType</a>
</td>
<td align="left" width="63%">
Binds to the type descriptions contained within a type library.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>