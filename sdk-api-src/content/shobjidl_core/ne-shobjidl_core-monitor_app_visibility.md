---
UID: NE:shobjidl_core.MONITOR_APP_VISIBILITY
title: MONITOR_APP_VISIBILITY
author: windows-sdk-content
description: Specifies whether a display is showing desktop windows instead of Windows Store apps.
old-location: shell\MONITOR_APP_VISIBILITY.htm
old-project: shell
ms.assetid: DE52080C-5EC3-489B-ACC8-D5EAEE3DDF78
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MAV_APP_VISIBLE, MAV_NO_APP_VISIBLE, MAV_UNKNOWN, MONITOR_APP_VISIBILITY, MONITOR_APP_VISIBILITY enumeration [Windows Shell], shell.MONITOR_APP_VISIBILITY, shobjidl_core/MAV_APP_VISIBLE, shobjidl_core/MAV_NO_APP_VISIBLE, shobjidl_core/MAV_UNKNOWN, shobjidl_core/MONITOR_APP_VISIBILITY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MONITOR_APP_VISIBILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - MONITOR_APP_VISIBILITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# MONITOR_APP_VISIBILITY enumeration


## -description


Specifies whether a display is showing desktop windows instead of Windows Store apps.


## -enum-fields




### -field MAV_UNKNOWN

The display state is not known.


### -field MAV_NO_APP_VISIBLE

The display is showing desktop windows.


### -field MAV_APP_VISIBLE

The display is not showing desktop windows.


## -remarks



The <b>MONITOR_APP_VISIBILITY</b> enum is used by the <a href="https://msdn.microsoft.com/F03AEE1F-1156-4565-871E-4C8CB5C4EDCA">GetAppVisibilityOnMonitor</a> method.




## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>
 

 

