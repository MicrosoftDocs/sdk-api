---
UID: NN:shappmgr.IPublishedApp
title: IPublishedApp (shappmgr.h)
description: Exposes methods that represent applications to Add/Remove Programs in Control Panel.
helpviewer_keywords: ["IPublishedApp","IPublishedApp interface [Windows Shell]","IPublishedApp interface [Windows Shell]","described","inet_IPublishedApp","shappmgr/IPublishedApp","shell.IPublishedApp"]
old-location: shell\IPublishedApp.htm
tech.root: shell
ms.assetid: a5a44e74-494a-4c9b-8bf3-85c6093b2c0e
ms.date: 12/05/2018
ms.keywords: IPublishedApp, IPublishedApp interface [Windows Shell], IPublishedApp interface [Windows Shell],described, inet_IPublishedApp, shappmgr/IPublishedApp, shell.IPublishedApp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPublishedApp
 - shappmgr/IPublishedApp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp
---

# IPublishedApp interface


## -description

Exposes methods that represent applications to Add/Remove Programs in Control Panel.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublishedApp</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>. <b>IPublishedApp</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">GetPublishedAppInfo</a>
</td>
<td align="left" width="63%">
Gets publishing-related information about an application published by an application publisher.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-install">Install</a>
</td>
<td align="left" width="63%">
Installs an application published by an application publisher. This method is invoked when the user selects <b>Add</b> or <b>Add Later</b> in Add/Remove Programs in Control Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-unschedule">Unschedule</a>
</td>
<td align="left" width="63%">
Cancels the installation of an application published by an application publisher.

</td>
</tr>
</table>

## -remarks

To publish applications to Add/Remove Programs in Control Panel, you must support <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a> and <b>IPublishedApp</b>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>

