---
UID: NF:shobjidl_core.IAppVisibilityEvents.AppVisibilityOnMonitorChanged
title: IAppVisibilityEvents::AppVisibilityOnMonitorChanged
author: windows-sdk-content
description: Notifies a client that the mode of a display has changed.
old-location: shell\IAppVisibilityEvents_AppVisibilityOnMonitorChanged.htm
old-project: shell
ms.assetid: a3fe5a6b-bb8b-4a9d-9ae2-529cce1291ad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AppVisibilityOnMonitorChanged, AppVisibilityOnMonitorChanged method [Windows Shell], AppVisibilityOnMonitorChanged method [Windows Shell],IAppVisibilityEvents interface, IAppVisibilityEvents interface [Windows Shell],AppVisibilityOnMonitorChanged method, IAppVisibilityEvents.AppVisibilityOnMonitorChanged, IAppVisibilityEvents::AppVisibilityOnMonitorChanged, shell.IAppVisibilityEvents_AppVisibilityOnMonitorChanged, shobjidl_core/IAppVisibilityEvents::AppVisibilityOnMonitorChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - twinapi.lib
 - twinapi.dll
api_name:
 - IAppVisibilityEvents.AppVisibilityOnMonitorChanged
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAppVisibilityEvents::AppVisibilityOnMonitorChanged


## -description


Notifies a client that the mode of a display has changed.


## -parameters




### -param hMonitor [in]

The display that has a changing mode.


### -param previousMode [in]

The previous mode of <i>hMonitor</i>, which may be <b>MAV_UNKNOWN</b>  if the client was unaware of the display previously.


### -param currentMode [in]

The current mode of <i>hMonitor</i>, which will not be <b>MAV_UNKNOWN</b>.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/F6BABF7D-FA05-4A68-878F-A27A6990EC3F">IAppVisibilityEvents</a>
 

 

