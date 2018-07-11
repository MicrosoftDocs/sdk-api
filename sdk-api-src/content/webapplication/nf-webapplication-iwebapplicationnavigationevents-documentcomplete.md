---
UID: NF:webapplication.IWebApplicationNavigationEvents.DocumentComplete
title: IWebApplicationNavigationEvents::DocumentComplete
author: windows-sdk-content
description: Fired when the document being navigated to reaches ReadyState_Complete.
old-location: debug\iwebapplicationnavigationevents_documentcomplete.htm
old-project: debug_wwahost
ms.assetid: 18dabd8a-d35c-4095-985d-bf712c539df8
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: DocumentComplete, DocumentComplete method [Debugging Windows Store apps], DocumentComplete method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, IWebApplicationNavigationEvents interface [Debugging Windows Store apps],DocumentComplete method, IWebApplicationNavigationEvents.DocumentComplete, IWebApplicationNavigationEvents::DocumentComplete, debug.iwebapplicationnavigationevents_documentcomplete, webapplication/IWebApplicationNavigationEvents::DocumentComplete
ms.prod: windows
ms.technology: windows-sdk
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
 - IWebApplicationNavigationEvents.DocumentComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWebApplicationNavigationEvents::DocumentComplete


## -description


Fired when the document being navigated to reaches ReadyState_Complete.


## -parameters




### -param htmlWindow [in]

Type: <b><a href="_inet_IHTMLWindow2_Interface">IHTMLWindow2</a>*</b>

The window or frame in which the document is loaded.


### -param url [in]

Type: <b>LPCWSTR</b>

The URL of the document.


## -returns



Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/580d4b21-3a4b-4e0c-b0d1-25b4e4fb2b1b">IWebApplicationNavigationEvents</a>
 

 

