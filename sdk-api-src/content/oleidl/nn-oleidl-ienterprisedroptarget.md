---
UID: NN:oleidl.IEnterpriseDropTarget
title: IEnterpriseDropTarget (oleidl.h)
description: When implemented by the drop target application, this interface gives the OLE drag and drop engine the ability to determine whether the drop target application intends to evaluate enterprise protection policy and gives the OLE drag and drop engine a way to provide the enterprise ID of the drop source application to the drop target application.
helpviewer_keywords: ["IEnterpriseDropTarget","IEnterpriseDropTarget interface [COM]","IEnterpriseDropTarget interface [COM]","described","com.ienterprisedroptarget","oleidl/IEnterpriseDropTarget"]
old-location: com\ienterprisedroptarget.htm
tech.root: com
ms.assetid: 9ACFE824-5F0D-42CC-8E2F-DF2658AC9908
ms.date: 12/05/2018
ms.keywords: IEnterpriseDropTarget, IEnterpriseDropTarget interface [COM], IEnterpriseDropTarget interface [COM],described, com.ienterprisedroptarget, oleidl/IEnterpriseDropTarget
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IEnterpriseDropTarget
 - oleidl/IEnterpriseDropTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IEnterpriseDropTarget
---

# IEnterpriseDropTarget interface


## -description

When implemented by the drop target application, this interface gives the OLE drag and drop engine the ability to determine whether the drop target application intends to evaluate enterprise protection policy and gives the OLE drag and drop engine a way to provide the enterprise ID of the drop source application to the drop target application.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnterpriseDropTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnterpriseDropTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnterpriseDropTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ienterprisedroptarget-isevaluatingedppolicy">IsEvaluatingEdpPolicy</a>
</td>
<td align="left" width="63%">
Indicates whether the drop target is evaluating the enterprise protection policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ienterprisedroptarget-setdropsourceenterpriseid">SetDropSourceEnterpriseid</a>
</td>
<td align="left" width="63%">
Provides the drop target with the enterprise ID of the drop source.

</td>
</tr>
</table>