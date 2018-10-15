---
UID: NN:shappmgr.IEnumPublishedApps
title: IEnumPublishedApps
author: windows-sdk-content
description: Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through IAppPublisher::EnumApps.
old-location: shell\IEnumPublishedApps.htm
tech.root: shell
ms.assetid: 89a06b1d-1b72-46ca-91cd-bb63ea0cbff7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnumPublishedApps, IEnumPublishedApps interface [Windows Shell], IEnumPublishedApps interface [Windows Shell],described, inet_IEnumPublishedApps, shappmgr/IEnumPublishedApps, shell.IEnumPublishedApps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - Shappmgr.h
api_name:
 - IEnumPublishedApps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPublishedApps interface


## -description


Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through <a href="https://msdn.microsoft.com/b24c3007-662a-4c42-9ca7-367180152deb">IAppPublisher::EnumApps</a>.  
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPublishedApps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPublishedApps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPublishedApps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78d18529-2eeb-4510-8703-457ffe998bc5">Next</a>
</td>
<td align="left" width="63%">
Gets the next <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> object in the enumeration.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/007f6636-725a-4af5-ad3f-578f8183a088">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration of <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> objects to the first item.
		

</td>
</tr>
</table> 


## -remarks



To publish applications to Add/Remove Programs in the Control Panel, you must support <b>IEnumPublishedApps</b>, <a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a> and <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>
 

 

