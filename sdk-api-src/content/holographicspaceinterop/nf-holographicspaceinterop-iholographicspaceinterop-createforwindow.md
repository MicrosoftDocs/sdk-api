---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


### -param holographicSpace






#### - **holographicSpace [out]

Address of a pointer to a <a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">HolographicSpace</a> object.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/119299C1-ECD9-46BA-B499-66890225E4E0">IHolographicSpaceInterop</a>



<a href="https://developer.microsoft.com/windows/mixed-reality">Mixed Reality Dev Center</a>



<a href="https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace">WinRT reference documentation</a>
 

 

