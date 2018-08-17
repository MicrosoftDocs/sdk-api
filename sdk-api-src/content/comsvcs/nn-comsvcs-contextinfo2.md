---
UID: NN:comsvcs.ContextInfo2
title: ContextInfo2
author: windows-sdk-content
description: Provides additional information about an object's context, supplementing the information that is available through the ContextInfo interface.
old-location: cos\contextinfo2.htm
old-project: cossdk
ms.assetid: 06954cc5-19a7-4bae-ac30-94dcdc35d15d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ContextInfo2, ContextInfo2 interface [COM+], ContextInfo2 interface [COM+],described, _cos_ContextInfo2, comsvcs/ContextInfo2, cos.contextinfo2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - ContextInfo2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ContextInfo2 interface


## -description


 Provides additional information about an object's context, supplementing the information that is available through the <a href="https://msdn.microsoft.com/en-us/library/ms687780(v=VS.85).aspx">ContextInfo</a> interface.

<b>ContextInfo2</b> and <a href="https://msdn.microsoft.com/en-us/library/ms679257(v=VS.85).aspx">IObjectContextInfo2</a> provide the same functionality, but unlike <b>IObjectContextInfo2</b>, <b>ContextInfo2</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ContextInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms687780(v=VS.85).aspx">ContextInfo</a>. <b>ContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms685065(v=VS.85).aspx">GetApplicationId</a>
</td>
<td align="left" width="63%">
 Retrieves the GUID of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682799(v=VS.85).aspx">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686048(v=VS.85).aspx">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the COM+ partition of the current object context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688501(v=VS.85).aspx">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687780(v=VS.85).aspx">ContextInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684253(v=VS.85).aspx">IObjectContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679257(v=VS.85).aspx">IObjectContextInfo2</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678909(v=VS.85).aspx">ObjectContext</a>
 

 

