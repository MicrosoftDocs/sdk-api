---
UID: NN:oaidl.ISupportErrorInfo
title: ISupportErrorInfo (oaidl.h)
description: Ensures that error information can be propagated up the call chain correctly. Automation objects that use the error handling interfaces must implement ISupportErrorInfo.
helpviewer_keywords: ["ISupportErrorInfo","ISupportedErrorInfo","ISupportedErrorInfo interface [Automation]","ISupportedErrorInfo interface [Automation]","described","_oa96_ISupportErrorInfo_Interface","automat.isupporterrorinfo","oaidl/ISupportErrorInfo"]
old-location: automat\isupporterrorinfo.htm
tech.root: automat
ms.assetid: 42d33066-36b4-4a5b-aa5d-46682e560f32
ms.date: 12/05/2018
ms.keywords: ISupportErrorInfo, ISupportedErrorInfo, ISupportedErrorInfo interface [Automation], ISupportedErrorInfo interface [Automation],described, _oa96_ISupportErrorInfo_Interface, automat.isupporterrorinfo, oaidl/ISupportErrorInfo
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
 - ISupportErrorInfo
 - oaidl/ISupportErrorInfo
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
 - ISupportedErrorInfo
---

# ISupportErrorInfo interface


## -description

Ensures that error information can be propagated up the call chain correctly. Automation objects that use the error handling interfaces must implement <b>ISupportErrorInfo</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISupportedErrorInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISupportErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISupportedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo">InterfaceSupportsErrorInfo</a>
</td>
<td align="left" width="63%">
Indicates whether an interface supports the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a> interface.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/automat/error-handling-interfaces">Error Handling Interfaces </a>