---
UID: NF:webapplication.IWebApplicationUIEvents.SecurityProblem
title: IWebApplicationUIEvents::SecurityProblem (webapplication.h)
description: Notifies the authoring app about an authentication problem.
helpviewer_keywords: ["IWebApplicationUIEvents interface [Debugging Windows Store apps]","SecurityProblem method","IWebApplicationUIEvents.SecurityProblem","IWebApplicationUIEvents::SecurityProblem","SecurityProblem","SecurityProblem method [Debugging Windows Store apps]","SecurityProblem method [Debugging Windows Store apps]","IWebApplicationUIEvents interface","debug.iwebapplicationuievents_securityproblem","webapplication/IWebApplicationUIEvents::SecurityProblem"]
old-location: debug\iwebapplicationuievents_securityproblem.htm
tech.root: debug_wwahost
ms.assetid: 3579ffe7-914c-4baf-b1bf-4ed1a1db645f
ms.date: 12/05/2018
ms.keywords: IWebApplicationUIEvents interface [Debugging Windows Store apps],SecurityProblem method, IWebApplicationUIEvents.SecurityProblem, IWebApplicationUIEvents::SecurityProblem, SecurityProblem, SecurityProblem method [Debugging Windows Store apps], SecurityProblem method [Debugging Windows Store apps],IWebApplicationUIEvents interface, debug.iwebapplicationuievents_securityproblem, webapplication/IWebApplicationUIEvents::SecurityProblem
f1_keywords:
- webapplication/IWebApplicationUIEvents.SecurityProblem
dev_langs:
- c++
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
- IWebApplicationUIEvents.SecurityProblem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebApplicationUIEvents::SecurityProblem


## -description


Notifies the authoring app about an authentication problem.


## -parameters




### -param securityProblem [in]

Type: <b>DWORD</b>

The security problem encountered.


### -param result [out]

Type: <b>HRESULT*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationuievents">IWebApplicationUIEvents</a>
 

 

