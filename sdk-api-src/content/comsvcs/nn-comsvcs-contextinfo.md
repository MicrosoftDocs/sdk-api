---
UID: NN:comsvcs.ContextInfo
title: ContextInfo (comsvcs.h)

description: Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.
old-location: cos\contextinfo.htm
tech.root: cossdk
ms.assetid: ef8d7ef7-fae4-4a20-80fb-18f5daa9b564

ms.date: 12/05/2018
ms.keywords: ContextInfo, ContextInfo interface [COM+], ContextInfo interface [COM+],described, _cos_ContextInfo, comsvcs/ContextInfo, cos.contextinfo
ms.topic: interface
f1_keywords: 
 - "comsvcs/ContextInfo"
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
 - ContextInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ContextInfo interface


## -description


Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

<b>ContextInfo</b> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a> provide the same functionality, but unlike <b>IObjectContextInfo</b>, <b>ContextInfo</b> is compatible with Automation.

In COM+ 1.5, released with Windows XP, the <b>ContextInfo</b> interface is superseded by the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo2">ContextInfo2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ContextInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ContextInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ContextInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo-getactivityid">GetActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the activity identifier associated with the object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo-getcontextid">GetContextId</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier of this object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo-gettransaction">GetTransaction</a>
</td>
<td align="left" width="63%">
Retrieves the object context's transaction object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo-gettransactionid">GetTransactionId</a>
</td>
<td align="left" width="63%">
Retrieves the transaction identifier associated with the object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-contextinfo-isintransaction">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
 

 

