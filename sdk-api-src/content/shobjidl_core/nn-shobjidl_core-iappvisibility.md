---
UID: NN:shobjidl_core.IAppVisibility
title: IAppVisibility
author: windows-sdk-content
description: Provides functionality to determine whether the display is showing Windows Store apps.
old-location: shell\IAppVisibility.htm
old-project: shell
ms.assetid: 89E26D36-3536-45F5-9396-83CCFB26890B
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAppVisibility, IAppVisibility interface [Windows Shell], IAppVisibility interface [Windows Shell],described, shell.IAppVisibility, shobjidl_core/IAppVisibility
ms.prod: windows
ms.technology: windows-sdk
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
-	shobjidl_core.h
api_name:
-	IAppVisibility
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAppVisibility interface


## -description


Provides functionality to determine whether the display is showing Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppVisibility</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppVisibility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppVisibility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602F46EF-014C-4219-9C1F-C1B4371EA456">Advise</a>
</td>
<td align="left" width="63%">
Registers an advise sink object to receive notification of changes to the display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F03AEE1F-1156-4565-871E-4C8CB5C4EDCA">GetAppVisibilityOnMonitor</a>
</td>
<td align="left" width="63%">
Queries the current mode of the specified monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D7BBAEC-A745-4707-861E-74CC331ED356">IsLauncherVisible</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the Start screen is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D670F1E7-5E0B-498E-8F27-DF2A3A387862">Unadvise</a>
</td>
<td align="left" width="63%">
Cancels a connection that was previously established by using <a href="https://msdn.microsoft.com/602F46EF-014C-4219-9C1F-C1B4371EA456">Advise</a>.

</td>
</tr>
</table> 


## -remarks



Use the <b>IAppVisibility</b> interface to determine when a display is showing Windows Store apps. This is useful for accessibility tools and other applications.

Use the <a href="https://msdn.microsoft.com/8D7BBAEC-A745-4707-861E-74CC331ED356">IsLauncherVisible</a>  method to determine when  the Start screen is visible.

Don't implement the <b>IAppVisibility</b> interface. Instead, call the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function with <b>CLSID_AppVisibility</b>.




## -see-also




<a href="https://msdn.microsoft.com/F6BABF7D-FA05-4A68-878F-A27A6990EC3F">IAppVisibilityEvents</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/DE52080C-5EC3-489B-ACC8-D5EAEE3DDF78">MONITOR_APP_VISIBILITY</a>
 

 

