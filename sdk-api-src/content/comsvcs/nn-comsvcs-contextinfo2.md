---
UID: NN:comsvcs.ContextInfo2
title: ContextInfo2 (comsvcs.h)
description: Provides additional information about an object's context, supplementing the information that is available through the ContextInfo interface.
helpviewer_keywords: ["ContextInfo2","ContextInfo2 interface [COM+]","ContextInfo2 interface [COM+]","described","_cos_ContextInfo2","comsvcs/ContextInfo2","cos.contextinfo2"]
old-location: cos\contextinfo2.htm
tech.root: cos
ms.assetid: 06954cc5-19a7-4bae-ac30-94dcdc35d15d
ms.date: 12/05/2018
ms.keywords: ContextInfo2, ContextInfo2 interface [COM+], ContextInfo2 interface [COM+],described, _cos_ContextInfo2, comsvcs/ContextInfo2, cos.contextinfo2
f1_keywords:
- comsvcs/ContextInfo2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- ContextInfo2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ContextInfo2 interface


## -description


 Provides additional information about an object's context, supplementing the information that is available through the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a> interface.

<b>ContextInfo2</b> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a> provide the same functionality, but unlike <b>IObjectContextInfo2</b>, <b>ContextInfo2</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ContextInfo2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>. <b>ContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ContextInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo2-getapplicationid">GetApplicationId</a>
</td>
<td align="left" width="63%">
 Retrieves the GUID of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo2-getapplicationinstanceid">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo2-getpartitionid">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the COM+ partition of the current object context.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--partitions">COM+ Partitions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
 

 

