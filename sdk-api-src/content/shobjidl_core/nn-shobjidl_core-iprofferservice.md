---
UID: NN:shobjidl_core.IProfferService
title: IProfferService
author: windows-sdk-content
description: Exposes a general mechanism for objects to offer services to other objects on the same host.
old-location: shell\IProfferService.htm
tech.root: shell
ms.assetid: 91aa5f9a-c276-4822-93e1-9cd2c48ddd9f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IProfferService, IProfferService interface [Windows Shell], IProfferService interface [Windows Shell],described, inet_IProfferService, shell.IProfferService, shobjidl_core/IProfferService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - IProfferService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProfferService interface


## -description


Exposes a general mechanism for objects to offer services to other objects on the same host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProfferService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProfferService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProfferService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">ProfferService</a>
</td>
<td align="left" width="63%">
Makes a service available to other objects on the same host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90868bbb-6fcd-4de1-a853-524542b74701">RevokeService</a>
</td>
<td align="left" width="63%">
Makes a service unavailable that had previously been available to other objects through <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.
		

</td>
</tr>
</table> 


## -remarks



Objects that expose a service first call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on their host for this interface, then execute <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a>
 

 

