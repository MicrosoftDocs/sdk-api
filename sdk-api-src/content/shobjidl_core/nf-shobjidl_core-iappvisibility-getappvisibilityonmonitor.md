---
UID: NF:shobjidl_core.IAppVisibility.GetAppVisibilityOnMonitor
title: IAppVisibility::GetAppVisibilityOnMonitor (shobjidl_core.h)
description: Queries the current mode of the specified monitor.
helpviewer_keywords: ["GetAppVisibilityOnMonitor","GetAppVisibilityOnMonitor method [Windows Shell]","GetAppVisibilityOnMonitor method [Windows Shell]","IAppVisibility interface","IAppVisibility interface [Windows Shell]","GetAppVisibilityOnMonitor method","IAppVisibility.GetAppVisibilityOnMonitor","IAppVisibility::GetAppVisibilityOnMonitor","shell.IAppVisibility_GetAppVisibilityOnMonitor","shobjidl_core/IAppVisibility::GetAppVisibilityOnMonitor"]
old-location: shell\IAppVisibility_GetAppVisibilityOnMonitor.htm
tech.root: shell
ms.assetid: F03AEE1F-1156-4565-871E-4C8CB5C4EDCA
ms.date: 12/05/2018
ms.keywords: GetAppVisibilityOnMonitor, GetAppVisibilityOnMonitor method [Windows Shell], GetAppVisibilityOnMonitor method [Windows Shell],IAppVisibility interface, IAppVisibility interface [Windows Shell],GetAppVisibilityOnMonitor method, IAppVisibility.GetAppVisibilityOnMonitor, IAppVisibility::GetAppVisibilityOnMonitor, shell.IAppVisibility_GetAppVisibilityOnMonitor, shobjidl_core/IAppVisibility::GetAppVisibilityOnMonitor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppVisibility::GetAppVisibilityOnMonitor
 - shobjidl_core/IAppVisibility::GetAppVisibilityOnMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility.GetAppVisibilityOnMonitor
---

# IAppVisibility::GetAppVisibilityOnMonitor


## -description

Queries the current mode of the specified monitor.

## -parameters

### -param hMonitor [in]

The monitor to query.

### -param pMode [out]

The current mode of <i>hMonitor</i>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pMode</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility">MONITOR_APP_VISIBILITY</a>