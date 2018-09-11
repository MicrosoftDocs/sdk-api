---
UID: NN:comsvcs.IServiceCall
title: IServiceCall
author: windows-sdk-content
description: Used to implement the batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iservicecall.htm
tech.root: cossdk
ms.assetid: 97532e29-3d1a-4a7c-8103-dd7ae2866a70
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IServiceCall, IServiceCall interface [COM+], IServiceCall interface [COM+],described, _cos_IServiceCall, comsvcs/IServiceCall, cos.iservicecall
ms.prod: windows
ms.technology: windows-sdk
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
 - IServiceCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceCall interface


## -description


Used to implement the batch work that is submitted through the activity created by <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceCall</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServiceCall</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IServiceCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678912(v=VS.85).aspx">OnCall</a>
</td>
<td align="left" width="63%">
Triggers the execution of the batch work implemented in this method.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683598(v=VS.85).aspx">IAsyncErrorNotify</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678822(v=VS.85).aspx">IServiceActivity</a>
 

 

