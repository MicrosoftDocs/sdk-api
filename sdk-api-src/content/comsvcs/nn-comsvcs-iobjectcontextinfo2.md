---
UID: NN:comsvcs.IObjectContextInfo2
title: IObjectContextInfo2 (comsvcs.h)
description: Provides additional information about an object's context. This interface extends the IObjectContextInfo interface.
helpviewer_keywords: ["IObjectContextInfo2","IObjectContextInfo2 interface [COM+]","IObjectContextInfo2 interface [COM+]","described","_cos_IObjectContextInfo2","comsvcs/IObjectContextInfo2","cos.iobjectcontextinfo2"]
old-location: cos\iobjectcontextinfo2.htm
tech.root: cos
ms.assetid: 21e078d2-ba93-4118-b1d1-3b4b6e0e28a4
ms.date: 12/05/2018
ms.keywords: IObjectContextInfo2, IObjectContextInfo2 interface [COM+], IObjectContextInfo2 interface [COM+],described, _cos_IObjectContextInfo2, comsvcs/IObjectContextInfo2, cos.iobjectcontextinfo2
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IObjectContextInfo2
 - comsvcs/IObjectContextInfo2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectContextInfo2
---

# IObjectContextInfo2 interface


## -description

Provides additional information about an object's context. This interface extends the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo2</b> interface inherits from <b>IObjectContextInfo</b>. <b>IObjectContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectContextInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo2-getapplicationid">GetApplicationId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo2-getapplicationinstanceid">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo2-getpartitionid">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the partition of the current object context.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>