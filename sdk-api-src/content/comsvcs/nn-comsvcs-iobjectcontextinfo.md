---
UID: NN:comsvcs.IObjectContextInfo
title: IObjectContextInfo (comsvcs.h)
description: Retrieves transaction, activity, and context information on the current context object.helpviewer_keywords: ["IObjectContextInfo","IObjectContextInfo interface [COM+]","IObjectContextInfo interface [COM+]","described","_cos_IObjectContextInfo","comsvcs/IObjectContextInfo","cos.iobjectcontextinfo"]
old-location: cos\iobjectcontextinfo.htm
tech.root: cossdk
ms.assetid: 76dcc6f3-f840-4672-bba9-038c1249a306
ms.date: 12/05/2018
ms.keywords: IObjectContextInfo, IObjectContextInfo interface [COM+], IObjectContextInfo interface [COM+],described, _cos_IObjectContextInfo, comsvcs/IObjectContextInfo, cos.iobjectcontextinfo
f1_keywords:
- comsvcs/IObjectContextInfo
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- IObjectContextInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectContextInfo interface


## -description


Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

This interface has been superseded by the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContextInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectContextInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo-getactivityid">GetActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo-getcontextid">GetContextId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo-gettransaction">GetTransaction</a>
</td>
<td align="left" width="63%">
Retrieves a reference to the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo-gettransactionid">GetTransactionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextinfo-isintransaction">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>
 

 

