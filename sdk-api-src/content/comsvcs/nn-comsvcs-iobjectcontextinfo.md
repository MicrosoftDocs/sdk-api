---
UID: NN:comsvcs.IObjectContextInfo
title: IObjectContextInfo
author: windows-sdk-content
description: Retrieves transaction, activity, and context information on the current context object.
old-location: cos\iobjectcontextinfo.htm
old-project: cossdk
ms.assetid: 76dcc6f3-f840-4672-bba9-038c1249a306
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IObjectContextInfo, IObjectContextInfo interface [COM+], IObjectContextInfo interface [COM+],described, _cos_IObjectContextInfo, comsvcs/IObjectContextInfo, cos.iobjectcontextinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
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
req.lib: 
req.dll: 
req.irql: 
---

# IObjectContextInfo interface


## -description


Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

This interface has been superseded by the <a href="https://msdn.microsoft.com/en-us/library/ms679257(v=VS.85).aspx">IObjectContextInfo2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IObjectContextInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms686061(v=VS.85).aspx">GetActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684289(v=VS.85).aspx">GetContextId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687562(v=VS.85).aspx">GetTransaction</a>
</td>
<td align="left" width="63%">
Retrieves a reference to the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686455(v=VS.85).aspx">GetTransactionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683589(v=VS.85).aspx">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690084(v=VS.85).aspx">CoGetObjectContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679257(v=VS.85).aspx">IObjectContextInfo2</a>
 

 

