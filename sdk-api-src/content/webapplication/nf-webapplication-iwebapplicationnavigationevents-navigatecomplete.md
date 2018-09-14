---
UID: NF:webapplication.IWebApplicationNavigationEvents.NavigateComplete
title: IWebApplicationNavigationEvents::NavigateComplete
author: windows-sdk-content
description: Fired when the document being navigated to becomes visible and enters the navigation stack.
old-location: debug\iwebapplicationnavigationevents_navigatecomplete.htm
tech.root: debug_wwahost
ms.assetid: 51a80227-69ec-4f12-8d19-d2b932fbbfc0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWebApplicationNavigationEvents interface [Debugging Windows Store apps],NavigateComplete method, IWebApplicationNavigationEvents.NavigateComplete, IWebApplicationNavigationEvents::NavigateComplete, NavigateComplete, NavigateComplete method [Debugging Windows Store apps], NavigateComplete method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, debug.iwebapplicationnavigationevents_navigatecomplete, webapplication/IWebApplicationNavigationEvents::NavigateComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Webapplication.idl
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
 - webapplication.h
api_name:
 - IWebApplicationNavigationEvents.NavigateComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationNavigationEvents::NavigateComplete


## -description


Fired when the document being navigated to becomes visible and enters the navigation stack.


## -parameters




### -param htmlWindow [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa741505(v=VS.85).aspx">IHTMLWindow2</a>*</b>

The window or frame in which the navigation is occurred.


### -param url [in]

Type: <b>LPCWSTR</b>

The URL which was navigated to 


## -returns



Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b">IWebApplicationNavigationEvents</a>
 

 

