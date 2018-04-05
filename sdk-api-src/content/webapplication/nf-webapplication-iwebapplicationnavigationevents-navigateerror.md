---
UID: NF:webapplication.IWebApplicationNavigationEvents.NavigateError
title: IWebApplicationNavigationEvents::NavigateError method
author: windows-driver-content
description: Fired when a binding error occurs (window or frameset element).
old-location: debug\iwebapplicationnavigationevents_navigateerror.htm
old-project: debug_wwahost
ms.assetid: 1c6e34e8-e14f-4b6c-ad83-140a7141cf64
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWebApplicationNavigationEvents, IWebApplicationNavigationEvents interface [Debugging Windows Store apps], NavigateError method, IWebApplicationNavigationEvents::NavigateError, NavigateError method [Debugging Windows Store apps], NavigateError method [Debugging Windows Store apps], IWebApplicationNavigationEvents interface, NavigateError,IWebApplicationNavigationEvents.NavigateError, debug.iwebapplicationnavigationevents_navigateerror, webapplication/IWebApplicationNavigationEvents::NavigateError
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	webapplication.h
api_name:
-	IWebApplicationNavigationEvents.NavigateError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWebApplicationNavigationEvents::NavigateError method


## -description


Fired when a binding error occurs (window or frameset element).


## -parameters




### -param htmlWindow [in]

Type: <b><a href="_inet_IHTMLWindow2_Interface">IHTMLWindow2</a>*</b>

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
 

 

