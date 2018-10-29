---
UID: NN:shappmgr.IPublishedApp
title: IPublishedApp
author: windows-sdk-content
description: Exposes methods that represent applications to Add/Remove Programs in Control Panel.
old-location: shell\IPublishedApp.htm
tech.root: shell
ms.assetid: a5a44e74-494a-4c9b-8bf3-85c6093b2c0e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IPublishedApp, IPublishedApp interface [Windows Shell], IPublishedApp interface [Windows Shell],described, inet_IPublishedApp, shappmgr/IPublishedApp, shell.IPublishedApp
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
 - IPublishedApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPublishedApp interface


## -description


Exposes methods that represent applications to Add/Remove Programs in Control Panel.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublishedApp</b> interface inherits from <a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>. <b>IPublishedApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPublishedApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">GetPublishedAppInfo</a>
</td>
<td align="left" width="63%">
Gets publishing-related information about an application published by an application publisher.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d8c5720-b48f-4268-810c-c04b14d20d73">Install</a>
</td>
<td align="left" width="63%">
Installs an application published by an application publisher. This method is invoked when the user selects <b>Add</b> or <b>Add Later</b> in Add/Remove Programs in Control Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0d5a8cb-d382-4d7a-8d09-2dd153c03294">Unschedule</a>
</td>
<td align="left" width="63%">
Cancels the installation of an application published by an application publisher.

</td>
</tr>
</table> 


## -remarks



To publish applications to Add/Remove Programs in Control Panel, you must support <a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>, <a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a> and <b>IPublishedApp</b>.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

