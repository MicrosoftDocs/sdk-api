---
UID: NF:shobjidl_core.IAppVisibility.GetAppVisibilityOnMonitor
title: IAppVisibility::GetAppVisibilityOnMonitor
author: windows-sdk-content
description: Queries the current mode of the specified monitor.
old-location: shell\IAppVisibility_GetAppVisibilityOnMonitor.htm
old-project: shell
ms.assetid: F03AEE1F-1156-4565-871E-4C8CB5C4EDCA
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetAppVisibilityOnMonitor, GetAppVisibilityOnMonitor method [Windows Shell], GetAppVisibilityOnMonitor method [Windows Shell],IAppVisibility interface, IAppVisibility interface [Windows Shell],GetAppVisibilityOnMonitor method, IAppVisibility.GetAppVisibilityOnMonitor, IAppVisibility::GetAppVisibilityOnMonitor, shell.IAppVisibility_GetAppVisibilityOnMonitor, shobjidl_core/IAppVisibility::GetAppVisibilityOnMonitor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
-	IAppVisibility.GetAppVisibilityOnMonitor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>



<a href="https://msdn.microsoft.com/DE52080C-5EC3-489B-ACC8-D5EAEE3DDF78">MONITOR_APP_VISIBILITY</a>
 

 

