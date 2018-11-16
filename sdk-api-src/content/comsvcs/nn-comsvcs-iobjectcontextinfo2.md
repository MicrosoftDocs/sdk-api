---
UID: NN:comsvcs.IObjectContextInfo2
title: IObjectContextInfo2
author: windows-sdk-content
description: Provides additional information about an object's context. This interface extends the IObjectContextInfo interface.
old-location: cos\iobjectcontextinfo2.htm
tech.root: cossdk
ms.assetid: 21e078d2-ba93-4118-b1d1-3b4b6e0e28a4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IObjectContextInfo2, IObjectContextInfo2 interface [COM+], IObjectContextInfo2 interface [COM+],described, _cos_IObjectContextInfo2, comsvcs/IObjectContextInfo2, cos.iobjectcontextinfo2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IObjectContextInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContextInfo2 interface


## -description


Provides additional information about an object's context. This interface extends the <a href="https://msdn.microsoft.com/en-us/library/ms682798(v=VS.85).aspx">IObjectContextInfo</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo2</b> interface inherits from <b>IObjectContextInfo</b>. <b>IObjectContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms681164(v=VS.85).aspx">GetApplicationId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687117(v=VS.85).aspx">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678905(v=VS.85).aspx">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the partition of the current object context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms682798(v=VS.85).aspx">IObjectContextInfo</a>
 

 

