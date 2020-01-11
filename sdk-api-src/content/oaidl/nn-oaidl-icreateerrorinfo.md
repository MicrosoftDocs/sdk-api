---
UID: NN:oaidl.ICreateErrorInfo
title: ICreateErrorInfo (oaidl.h)
description: Returns error information.
old-location: automat\icreateerrorinfo.htm
tech.root: automat
ms.assetid: 2e7c5ad5-9018-413e-8826-ef752ebf302c
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo, ICreateErrorInfo interface [Automation], ICreateErrorInfo interface [Automation],described, _oa96_ICreateErrorInfo_Interface, automat.icreateerrorinfo, oaidl/ICreateErrorInfo
f1_keywords:
- oaidl/ICreateErrorInfo
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
- ICreateErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateErrorInfo interface


## -description


Returns error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Sets the textual description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-setguid">SetGUID</a>
</td>
<td align="left" width="63%">
Sets the globally unique identifier (GUID) of the interface that defined the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-sethelpcontext">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context identifier (ID) for the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-sethelpfile">SetHelpFile</a>
</td>
<td align="left" width="63%">
Sets the path of the Help file that describes the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/source">SetSource</a>
</td>
<td align="left" width="63%">
Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/error-handling-interfaces">Error Handling Interfaces </a>
 

 

