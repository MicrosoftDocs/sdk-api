---
UID: NN:restrictederrorinfo.ILanguageExceptionTransform
title: ILanguageExceptionTransform (restrictederrorinfo.h)
description: Allows language projections to make available to the system any and all context from an exception that gets thrown from the context of a catch handler that catches a different exception.
helpviewer_keywords: ["ILanguageExceptionTransform","ILanguageExceptionTransform interface [Windows Runtime]","ILanguageExceptionTransform interface [Windows Runtime]","described","restrictederrorinfo/ILanguageExceptionTransform","winrt.ilanguageexceptiontransform"]
old-location: winrt\ilanguageexceptiontransform.htm
tech.root: WinRT
ms.assetid: A42470EE-FA05-4716-BA17-009D59FEE259
ms.date: 12/05/2018
ms.keywords: ILanguageExceptionTransform, ILanguageExceptionTransform interface [Windows Runtime], ILanguageExceptionTransform interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionTransform, winrt.ilanguageexceptiontransform
f1_keywords:
- restrictederrorinfo/ILanguageExceptionTransform
dev_langs:
- c++
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
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
- restrictederrorinfo.h
api_name:
- ILanguageExceptionTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILanguageExceptionTransform interface


## -description


Allows language projections to make available to the system any and all context from an exception that gets thrown from the context of a catch handler that catches a different exception. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILanguageExceptionTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptiontransform-gettransformedrestrictederrorinfo">GetTransformedRestrictedErrorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the transformed restricted error info.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

