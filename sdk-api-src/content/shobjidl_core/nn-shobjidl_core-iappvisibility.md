---
UID: NN:shobjidl_core.IAppVisibility
title: IAppVisibility (shobjidl_core.h)

description: Provides functionality to determine whether the display is showing Windows Store apps.
old-location: shell\IAppVisibility.htm
tech.root: shell
ms.assetid: 89E26D36-3536-45F5-9396-83CCFB26890B

ms.date: 12/05/2018
ms.keywords: IAppVisibility, IAppVisibility interface [Windows Shell], IAppVisibility interface [Windows Shell],described, shell.IAppVisibility, shobjidl_core/IAppVisibility
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IAppVisibility"
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
 - IAppVisibility
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppVisibility interface


## -description


Provides functionality to determine whether the display is showing Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppVisibility</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppVisibility</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-advise">Advise</a>
</td>
<td align="left" width="63%">
Registers an advise sink object to receive notification of changes to the display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-getappvisibilityonmonitor">GetAppVisibilityOnMonitor</a>
</td>
<td align="left" width="63%">
Queries the current mode of the specified monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-islaunchervisible">IsLauncherVisible</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the Start screen is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Cancels a connection that was previously established by using <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-advise">Advise</a>.

</td>
</tr>
</table> 


## -remarks



Use the <b>IAppVisibility</b> interface to determine when a display is showing Windows Store apps. This is useful for accessibility tools and other applications.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-islaunchervisible">IsLauncherVisible</a>  method to determine when  the Start screen is visible.

Don't implement the <b>IAppVisibility</b> interface. Instead, call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function with <b>CLSID_AppVisibility</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents">IAppVisibilityEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility">MONITOR_APP_VISIBILITY</a>
 

 

