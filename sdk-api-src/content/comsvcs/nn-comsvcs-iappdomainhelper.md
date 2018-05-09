---
UID: NN:comsvcs.IAppDomainHelper
title: IAppDomainHelper
author: windows-driver-content
description: Binds a managed object to an application domain, which is an isolated environment where applications execute.
old-location: cos\iappdomainhelper.htm
old-project: cossdk
ms.assetid: 2709f284-ca8c-404e-b568-b655f780549a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IAppDomainHelper, IAppDomainHelper interface [COM+], IAppDomainHelper interface [COM+],described, _cos_IAppDomainHelper, comsvcs/IAppDomainHelper, cos.iappdomainhelper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IAppDomainHelper
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppDomainHelper interface


## -description


Binds a managed object to an application domain, which is an isolated environment where applications execute. It provides callbacks to enter an application domain and for shutdown of the application domain.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppDomainHelper</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAppDomainHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppDomainHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a82c2539-56cd-45ee-b673-a9440818bbc7">DoCallback</a>
</td>
<td align="left" width="63%">
Switches into a given application domain (which the calling object must be bound to), executes the supplied callback function in that application domain, and then returns to the original application domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Binds the calling object to the current application domain and provides a callback function for shutdown that is executed when the application domain is unloaded.

</td>
</tr>
</table> 

