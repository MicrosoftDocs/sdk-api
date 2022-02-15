---
UID: NF:webapplication.IWebApplicationScriptEvents.ScriptError
title: IWebApplicationScriptEvents::ScriptError (webapplication.h)
description: Fired when an unhandled script error occurs.
helpviewer_keywords: ["IWebApplicationScriptEvents interface [Debugging Windows Store apps]","ScriptError method","IWebApplicationScriptEvents.ScriptError","IWebApplicationScriptEvents::ScriptError","ScriptError","ScriptError method [Debugging Windows Store apps]","ScriptError method [Debugging Windows Store apps]","IWebApplicationScriptEvents interface","debug.iwebapplicationscriptevents_scripterror","webapplication/IWebApplicationScriptEvents::ScriptError"]
old-location: debug\iwebapplicationscriptevents_scripterror.htm
tech.root: debug
ms.assetid: 4f1e6260-804d-4881-b2d8-70a1463a46bd
ms.date: 12/05/2018
ms.keywords: IWebApplicationScriptEvents interface [Debugging Windows Store apps],ScriptError method, IWebApplicationScriptEvents.ScriptError, IWebApplicationScriptEvents::ScriptError, ScriptError, ScriptError method [Debugging Windows Store apps], ScriptError method [Debugging Windows Store apps],IWebApplicationScriptEvents interface, debug.iwebapplicationscriptevents_scripterror, webapplication/IWebApplicationScriptEvents::ScriptError
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWebApplicationScriptEvents::ScriptError
 - webapplication/IWebApplicationScriptEvents::ScriptError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - webapplication.h
api_name:
 - IWebApplicationScriptEvents.ScriptError
---

# IWebApplicationScriptEvents::ScriptError


## -description

Fired when an unhandled script error occurs.

## -parameters

### -param htmlWindow [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741505(v=vs.85)">IHTMLWindow2</a>*</b>

The window or frame in which the script error occurred.

### -param scriptError [in]

Type: <b><a href="/scripting/winscript/reference/iactivescripterror">IActiveScriptError</a>*</b>

The object that contains info about the script error that occurred.

### -param url [in]

Type: <b>LPCWSTR</b>

The URL on which the script error occurred.

### -param errorHandled [in]

Type: <b>BOOL</b>

<b>TRUE</b> if the app handled the error; otherwise <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationscriptevents">IWebApplicationScriptEvents</a>