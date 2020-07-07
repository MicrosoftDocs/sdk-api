---
UID: NN:shappmgr.IShellApp
title: IShellApp (shappmgr.h)
description: Exposes methods that provide general information about an application to the Add/Remove Programs Application.
helpviewer_keywords: ["IShellApp","IShellApp interface [Windows Shell]","IShellApp interface [Windows Shell]","described","inet_IShellApp","shappmgr/IShellApp","shell.IShellApp"]
old-location: shell\IShellApp.htm
tech.root: shell
ms.assetid: 2f56744c-a10e-423f-8b8f-c3257e560310
ms.date: 12/05/2018
ms.keywords: IShellApp, IShellApp interface [Windows Shell], IShellApp interface [Windows Shell],described, inet_IShellApp, shappmgr/IShellApp, shell.IShellApp
f1_keywords:
- shappmgr/IShellApp
dev_langs:
- c++
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
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellApp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellApp interface


## -description


Exposes methods that provide general information about an application to the Add/Remove Programs Application. You cannot use it outside the Add/Remove Programs application. The information given by this interface includes a list of supported management actions and whether the application is currently installed.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellApp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getappinfo">GetAppInfo</a>
</td>
<td align="left" width="63%">
Gets general information about an application.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getcachedslowappinfo">GetCachedSlowAppInfo</a>
</td>
<td align="left" width="63%">
Returns information to the application that originates from a slow source. Unlike <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getslowappinfo">IShellApp::GetSlowAppInfo</a>, this method can return information that has been cached. This method is not applicable to published applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getpossibleactions">GetPossibleActions</a>
</td>
<td align="left" width="63%">
Gets a bitmask of management actions allowed for an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getslowappinfo">GetSlowAppInfo</a>
</td>
<td align="left" width="63%">
Returns information to the application that originates from a slow source. This method is not applicable to published applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-isinstalled">IsInstalled</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether a specified application is currently installed.
		

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
 

 

