---
UID: NF:holographicspaceinterop.IHolographicSpaceInterop.CreateForWindow
title: IHolographicSpaceInterop::CreateForWindow
author: windows-sdk-content
description: Instantiates a HolographicSpace object and binds it to the current application.
old-location: mixedreality\iholographicspaceinterop_createforwindow.htm
tech.root: MixedReality
ms.assetid: 8B7A226E-FB47-4BA2-B13E-B37250C75920
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateForWindow, CreateForWindow method, CreateForWindow method,IHolographicSpaceInterop interface, IHolographicSpaceInterop interface,CreateForWindow method, IHolographicSpaceInterop.CreateForWindow, IHolographicSpaceInterop::CreateForWindow, MixedReality.iholographicspaceinterop_createforwindow, holographicspaceinterop/IHolographicSpaceInterop::CreateForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: holographicspaceinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: HolographicSpaceInterop.idl
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
 - HolographicSpaceInterop.h
api_name:
 - IHolographicSpaceInterop.CreateForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHolographicSpaceInterop::CreateForWindow


## -description


[ 
        Updated for UWP apps on Windows 10. For Windows 8.x articles, see the
        <a href="http://go.microsoft.com/fwlink/p/?linkid=619132">archive</a> ]

Instantiates a <a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">HolographicSpace</a> object and binds it to the current application.


## -parameters




### -param window [in]

Handle to the windows of the active application.


### -param riid [in]

The RUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(IRadialController) will get the GUID of the interface to a buffer resource.


### -param holographicSpace [out]

Address of a pointer to a <a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">HolographicSpace</a> object.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/119299C1-ECD9-46BA-B499-66890225E4E0">IHolographicSpaceInterop</a>



<a href="https://developer.microsoft.com/windows/mixed-reality">Mixed Reality Dev Center</a>



<a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">WinRT reference documentation</a>
 

 

