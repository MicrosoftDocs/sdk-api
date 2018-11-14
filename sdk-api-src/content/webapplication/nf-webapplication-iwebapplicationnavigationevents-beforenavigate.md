---
UID: NF:webapplication.IWebApplicationNavigationEvents.BeforeNavigate
title: IWebApplicationNavigationEvents::BeforeNavigate
author: windows-sdk-content
description: Fired before navigate occurs in the given host (window or frameset element).
old-location: debug\iwebapplicationnavigationevents_beforenavigate.htm
tech.root: debug_wwahost
ms.assetid: 1088bfa3-0a20-4156-90ff-50129e903052
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BeforeNavigate, BeforeNavigate method [Debugging Windows Store apps], BeforeNavigate method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, IWebApplicationNavigationEvents interface [Debugging Windows Store apps],BeforeNavigate method, IWebApplicationNavigationEvents.BeforeNavigate, IWebApplicationNavigationEvents::BeforeNavigate, debug.iwebapplicationnavigationevents_beforenavigate, webapplication/IWebApplicationNavigationEvents::BeforeNavigate
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
 - IWebApplicationNavigationEvents.BeforeNavigate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- webapplication.h
: 
- IWebApplicationNavigationEvents.BeforeNavigate
: 
---

# IWebApplicationNavigationEvents::BeforeNavigate


## -description


Fired before navigate occurs in the given host (window or frameset element).


## -parameters




### -param htmlWindow [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa741505(v=VS.85).aspx">IHTMLWindow2</a>*</b>

The window or frame in which the navigation is about occur.


### -param url [in]

Type: <b>LPCWSTR</b>

The URL to navigate to.


### -param navigationFlags [in]

Type: <b>DWORD</b>

Flags related to the current navigation.


### -param targetFrameName [in]

Type: <b>LPCWSTR</b>

The name of the frame in which the navigation is about to occur. The value is <b>null</b> if no named frame is targeted.


## -returns



Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b">IWebApplicationNavigationEvents</a>
 

 

