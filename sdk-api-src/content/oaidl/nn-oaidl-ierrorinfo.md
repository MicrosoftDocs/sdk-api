---
UID: NN:oaidl.IErrorInfo
title: IErrorInfo (oaidl.h)
description: Provides detailed contextual error information.helpviewer_keywords: ["IErrorInfo","IErrorInfo interface [Automation]","IErrorInfo interface [Automation]","described","_oa96_IErrorInfo_Interface","automat.ierrorinfo","oaidl/IErrorInfo"]
old-location: automat\ierrorinfo.htm
tech.root: automat
ms.assetid: 4dda6909-2d9a-4727-ae0c-b5f90dcfa447
ms.date: 12/05/2018
ms.keywords: IErrorInfo, IErrorInfo interface [Automation], IErrorInfo interface [Automation],described, _oa96_IErrorInfo_Interface, automat.ierrorinfo, oaidl/IErrorInfo
f1_keywords:
- oaidl/IErrorInfo
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
- IErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IErrorInfo interface


## -description


Provides detailed contextual error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a textual description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-getguid">GetGUID</a>
</td>
<td align="left" width="63%">
Returns the globally unique identifier (GUID) of the interface that defined the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-gethelpcontext">GetHelpContext</a>
</td>
<td align="left" width="63%">
Returns the Help context identifier (ID) for the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-gethelpfile">GetHelpFile</a>
</td>
<td align="left" width="63%">
Returns the path of the Help file that describes the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-getsource">GetSource</a>
</td>
<td align="left" width="63%">
Returns the language-dependent programmatic ID (ProgID) for the class or application that raised the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/error-handling-interfaces">Error Handling Interfaces </a>
 

 

