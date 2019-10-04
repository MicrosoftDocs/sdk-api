---
UID: NN:ndhelper.INetDiagHelperEx
title: INetDiagHelperEx (ndhelper.h)
author: windows-sdk-content
description: Provides methods that extend on the INetDiagHelper interface to capture and provide information associated with diagnoses and resolution of network-related issues.
old-location: ndf\inetdiaghelperex.htm
tech.root: NDF
ms.assetid: 9c03f24c-073f-40bc-aee7-c462d4e2d781
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetDiagHelperEx, INetDiagHelperEx interface [NDF], INetDiagHelperEx interface [NDF],described, ndf.inetdiaghelperex, ndhelper/INetDiagHelperEx
ms.topic: interface
f1_keywords: 
 - "ndhelper/INetDiagHelperEx"
dev_langs:
 - c++
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndhelper.idl
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
 - ndhelper.h
api_name:
 - INetDiagHelperEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetDiagHelperEx interface


## -description


The <b>INetDiagHelperEx</b> interface provides methods that extend on the <a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a> interface to capture and provide information associated with diagnoses and resolution of network-related issues.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetDiagHelperEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetDiagHelperEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetDiagHelperEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperex-reconfirmlowhealth">INetDiagHelperEx::ReconfirmLowHealth</a>
</td>
<td align="left" width="63%">
Adds a second Low Health pass after hypotheses have been diagnosed and before repairs are retrieved. This method is optional when building a Helper Class extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperex-reproducefailure">INetDiagHelperEx::ReproduceFailure</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperex-setutilities">INetDiagHelperEx::SetUtilities</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>
 

 

