---
UID: NF:spatialinteractionmanagerinterop.ISpatialInteractionManagerInterop.GetForWindow
title: ISpatialInteractionManagerInterop::GetForWindow
author: windows-sdk-content
description: Retrieves a SpatialInteractionManager object bound to the active application.
old-location: mixedreality\ispatialinteractionmanager_getforwindow.htm
tech.root: MixedReality
ms.assetid: 5D11BF4D-2EE3-40A3-A1EE-202DD5B904FE
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: GetForWindow, GetForWindow method, GetForWindow method,ISpatialInteractionManagerInterop interface, ISpatialInteractionManagerInterop interface,GetForWindow method, ISpatialInteractionManagerInterop.GetForWindow, ISpatialInteractionManagerInterop::GetForWindow, MixedReality.ispatialinteractionmanager_getforwindow, spatialinteractionmanagerinterop/ISpatialInteractionManagerInterop::GetForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialinteractionmanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SpatialInteractionManagerInterop.idl
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
 - SpatialInteractionManagerInterop.h
api_name:
 - ISpatialInteractionManagerInterop.GetForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialInteractionManagerInterop::GetForWindow


## -description


[ 
        Updated for UWP apps on Windows 10. For Windows 8.x articles, see the
        <a href="http://go.microsoft.com/fwlink/p/?linkid=619132">archive</a> ]

Retrieves a <a href="https://docs.microsoft.com/uwp/api/Windows.UI.Input.Spatial.SpatialInteractionManager">SpatialInteractionManager</a> object bound to the active application.


## -parameters




### -param window [in]

Handle to the window of the active application.


### -param riid [in]

The GUID of the <a href="https://docs.microsoft.com/uwp/api/Windows.UI.Input.Spatial.SpatialInteractionManager">SpatialInteractionManager</a> object.


### -param spatialInteractionManager

TBD




#### - **holographicSpace [out]

Address of a pointer to a <a href="https://docs.microsoft.com/uwp/api/Windows.UI.Input.Spatial.SpatialInteractionManager">SpatialInteractionManager</a> object.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="MixedReality.ispatialinteractionmanager">ISpatialInteractionManager</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt844796(v=WIN.10).aspx">ISpatialInteractionManagerInterop</a>



<a href="https://developer.microsoft.com/windows/mixed-reality">Mixed Reality Dev Center</a>



<a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">WinRT reference documentation</a>
 

 

