---
UID: NN:shappmgr.IEnumPublishedApps
title: IEnumPublishedApps (shappmgr.h)
author: windows-sdk-content
description: Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through IAppPublisher::EnumApps.
old-location: shell\IEnumPublishedApps.htm
tech.root: shell
ms.assetid: 89a06b1d-1b72-46ca-91cd-bb63ea0cbff7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumPublishedApps, IEnumPublishedApps interface [Windows Shell], IEnumPublishedApps interface [Windows Shell],described, inet_IEnumPublishedApps, shappmgr/IEnumPublishedApps, shell.IEnumPublishedApps
ms.topic: interface
f1_keywords: 
 - "shappmgr/IEnumPublishedApps"
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
ms.custom: 19H1
---

# IEnumPublishedApps interface


## -description


Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-enumapps">IAppPublisher::EnumApps</a>.  
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPublishedApps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPublishedApps</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ienumpublishedapps-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> object in the enumeration.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ienumpublishedapps-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration of <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> objects to the first item.
		

</td>
</tr>
</table> 


## -remarks



To publish applications to Add/Remove Programs in the Control Panel, you must support <b>IEnumPublishedApps</b>, <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
 

 

