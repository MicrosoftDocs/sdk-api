---
UID: NF:webapplication.IWebApplicationNavigationEvents.NavigateError
title: IWebApplicationNavigationEvents::NavigateError
author: windows-sdk-content
description: Fired when a binding error occurs (window or frameset element).
old-location: debug\iwebapplicationnavigationevents_navigateerror.htm
old-project: debug_wwahost
ms.assetid: 1c6e34e8-e14f-4b6c-ad83-140a7141cf64
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IWebApplicationNavigationEvents interface [Debugging Windows Store apps],NavigateError method, IWebApplicationNavigationEvents.NavigateError, IWebApplicationNavigationEvents::NavigateError, NavigateError, NavigateError method [Debugging Windows Store apps], NavigateError method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, debug.iwebapplicationnavigationevents_navigateerror, webapplication/IWebApplicationNavigationEvents::NavigateError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: webapplication.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - webapplication.h
api_name:
 - IWebApplicationNavigationEvents.NavigateError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWebApplicationNavigationEvents::NavigateError


## -description


Fired when a binding error occurs (window or frameset element).


## -parameters




### -param htmlWindow [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa741505(v=VS.85).aspx">IHTMLWindow2</a>*</b>

The window ro frame in which the navigation error occurred.


### -param url [in]

Type: <b>LPCWSTR</b>

The URL for which navigation failed.


### -param targetFrameName [in]

Type: <b>LPCWSTR</b>

The name of the frame in which the navigation error occurred. The value is <b>null</b> if no named frame was targeted.


### -param statusCode [in]

Type: <b>DWORD</b>

The error code. Could be a <b>HRESULT</b> or a HTTP status code. 


## -returns



Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b">IWebApplicationNavigationEvents</a>
 

 

