---
UID: NN:comsvcs.IObjectContextInfo
title: IObjectContextInfo
author: windows-sdk-content
description: Retrieves transaction, activity, and context information on the current context object.
old-location: cos\iobjectcontextinfo.htm
tech.root: cossdk
ms.assetid: 76dcc6f3-f840-4672-bba9-038c1249a306
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IObjectContextInfo, IObjectContextInfo interface [COM+], IObjectContextInfo interface [COM+],described, _cos_IObjectContextInfo, comsvcs/IObjectContextInfo, cos.iobjectcontextinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContextInfo interface


## -description


Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

This interface has been superseded by the <a href="https://msdn.microsoft.com/21e078d2-ba93-4118-b1d1-3b4b6e0e28a4">IObjectContextInfo2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectContextInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b6420f2e-223c-4a85-9c45-178a478c8424">GetActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97059f07-161f-451f-9f9b-b4dd81b7bf79">GetContextId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3a19d49-740a-436c-be6b-c98b5a14dc93">GetTransaction</a>
</td>
<td align="left" width="63%">
Retrieves a reference to the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8aa6fe8-acb2-4e00-a7fc-605bb56969e6">GetTransactionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8624e731-8296-4829-afae-fd48721a511c">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/97a0c6c3-a011-44dc-b428-aabdad7d4364">CoGetObjectContext</a>



<a href="https://msdn.microsoft.com/21e078d2-ba93-4118-b1d1-3b4b6e0e28a4">IObjectContextInfo2</a>
 

 

