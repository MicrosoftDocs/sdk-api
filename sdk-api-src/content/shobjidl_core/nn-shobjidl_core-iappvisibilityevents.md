---
UID: NN:shobjidl_core.IAppVisibilityEvents
title: IAppVisibilityEvents (shobjidl_core.h)
author: windows-sdk-content
description: Enables applications to receive notifications of state changes in a display and of changes in Start screen visibility.
old-location: shell\IAppVisibilityEvents.htm
tech.root: shell
ms.assetid: F6BABF7D-FA05-4A68-878F-A27A6990EC3F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppVisibilityEvents, IAppVisibilityEvents interface [Windows Shell], IAppVisibilityEvents interface [Windows Shell],described, shell.IAppVisibilityEvents, shobjidl_core/IAppVisibilityEvents
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IAppVisibilityEvents"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Twinapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - twinapi.lib
 - twinapi.dll
api_name:
 - IAppVisibilityEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppVisibilityEvents interface


## -description


Enables applications to receive notifications of state changes in a display and of changes in Start screen visibility.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppVisibilityEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppVisibilityEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppVisibilityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibilityevents-appvisibilityonmonitorchanged">AppVisibilityOnMonitorChanged</a>
</td>
<td align="left" width="63%">
Notifies a client that the mode of a display has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibilityevents-launchervisibilitychange">LauncherVisibilityChange</a>
</td>
<td align="left" width="63%">
Notifies a client that visibility of the Start screen has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

