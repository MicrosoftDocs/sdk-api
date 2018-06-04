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

# IWebApplicationScriptEvents::ScriptError


## -description


Fired when an unhandled script error occurs.


## -parameters




### -param htmlWindow [in]

Type: <b><a href="_inet_IHTMLWindow2_Interface">IHTMLWindow2</a>*</b>

The window or frame in which the script error occurred.


### -param scriptError [in]

Type: <b><a href="c8e0288d-38ff-4145-a7e3-f8cdfb72eefe">IActiveScriptError</a>*</b>

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
 

 

