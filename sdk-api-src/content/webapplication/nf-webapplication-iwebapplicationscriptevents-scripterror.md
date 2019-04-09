---
UID: NF:webapplication.IWebApplicationScriptEvents.ScriptError
title: IWebApplicationScriptEvents::ScriptError (webapplication.h)
author: windows-sdk-content
description: Fired when an unhandled script error occurs.
old-location: debug\iwebapplicationscriptevents_scripterror.htm
tech.root: debug_wwahost
ms.assetid: 4f1e6260-804d-4881-b2d8-70a1463a46bd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWebApplicationScriptEvents interface [Debugging Windows Store apps],ScriptError method, IWebApplicationScriptEvents.ScriptError, IWebApplicationScriptEvents::ScriptError, ScriptError, ScriptError method [Debugging Windows Store apps], ScriptError method [Debugging Windows Store apps],IWebApplicationScriptEvents interface, debug.iwebapplicationscriptevents_scripterror, webapplication/IWebApplicationScriptEvents::ScriptError
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
 - IWebApplicationScriptEvents.ScriptError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebApplicationScriptEvents::ScriptError


## -description


Fired when an unhandled script error occurs.


## -parameters




### -param htmlWindow [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa741505(v=VS.85).aspx">IHTMLWindow2</a>*</b>

The window or frame in which the script error occurred.


### -param scriptError [in]

Type: <b><a href="https://msdn.microsoft.com/library/b17d71fw(v=VS.85).aspx">IActiveScriptError</a>*</b>

The object that contains info about the script error that occurred.


### -param url [in]

Type: <b>LPCWSTR</b>

The URL on which the script error occurred.


### -param errorHandled [in]

Type: <b>BOOL</b>

<b>TRUE</b> if the app handled the error; otherwise <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a33f99a0-7c2d-45df-8a6a-d3257d537c9b">IWebApplicationScriptEvents</a>
 

 

