---
UID: NN:restrictederrorinfo.IRestrictedErrorInfo
title: IRestrictedErrorInfo (restrictederrorinfo.h)
description: Represents the details of an error, including restricted error information.helpviewer_keywords: ["IRestrictedErrorInfo","IRestrictedErrorInfo interface [Windows Runtime]","IRestrictedErrorInfo interface [Windows Runtime]","described","restrictederrorinfo/IRestrictedErrorInfo","winrt.irestrictederrorinfo"]
old-location: winrt\irestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: 1af8d4bf-1217-44ca-b0dd-9a6feda16100
ms.date: 12/05/2018
ms.keywords: IRestrictedErrorInfo, IRestrictedErrorInfo interface [Windows Runtime], IRestrictedErrorInfo interface [Windows Runtime],described, restrictederrorinfo/IRestrictedErrorInfo, winrt.irestrictederrorinfo
f1_keywords:
- restrictederrorinfo/IRestrictedErrorInfo
dev_langs:
- c++
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RestrictedErrorInfo.idl
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
- RestrictedErrorInfo.h
api_name:
- IRestrictedErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRestrictedErrorInfo interface


## -description


Represents the details of an error, including restricted error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRestrictedErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRestrictedErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRestrictedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-irestrictederrorinfo-geterrordetails">GetErrorDetails</a>
</td>
<td align="left" width="63%">
Returns information about an error, including the restricted error description.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-irestrictederrorinfo-getreference">GetReference</a>
</td>
<td align="left" width="63%">
Returns a reference to restricted error information. 

</td>
</tr>
</table> 

