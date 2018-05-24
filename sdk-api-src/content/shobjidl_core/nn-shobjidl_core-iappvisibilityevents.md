---
UID: NN:shobjidl_core.IAppVisibilityEvents
title: IAppVisibilityEvents
author: windows-driver-content
description: Enables applications to receive notifications of state changes in a display and of changes in Start screen visibility.
old-location: shell\IAppVisibilityEvents.htm
old-project: shell
ms.assetid: F6BABF7D-FA05-4A68-878F-A27A6990EC3F
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IAppVisibilityEvents, IAppVisibilityEvents interface [Windows Shell], IAppVisibilityEvents interface [Windows Shell],described, shell.IAppVisibilityEvents, shobjidl_core/IAppVisibilityEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	twinapi.lib
-	twinapi.dll
api_name:
-	IAppVisibilityEvents
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAppVisibilityEvents interface


## -description


Enables applications to receive notifications of state changes in a display and of changes in Start screen visibility.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppVisibilityEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppVisibilityEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a3fe5a6b-bb8b-4a9d-9ae2-529cce1291ad">AppVisibilityOnMonitorChanged</a>
</td>
<td align="left" width="63%">
Notifies a client that the mode of a display has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26789ef4-015a-4dfd-8265-e27b50c565c4">LauncherVisibilityChange</a>
</td>
<td align="left" width="63%">
Notifies a client that visibility of the Start screen has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

