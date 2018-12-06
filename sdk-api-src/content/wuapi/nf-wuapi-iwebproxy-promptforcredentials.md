---
UID: NF:wuapi.IWebProxy.PromptForCredentials
title: IWebProxy::PromptForCredentials
author: windows-sdk-content
description: Prompts the user for the password to use for proxy authentication.
old-location: wua\iwebproxy_promptforcredentials.htm
tech.root: wua_sdk
ms.assetid: 2eeb4418-d9fe-41b8-97c9-cafe18aab528
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWebProxy interface [Windows Update Agent],PromptForCredentials method, IWebProxy.PromptForCredentials, IWebProxy::PromptForCredentials, PromptForCredentials, PromptForCredentials method [Windows Update Agent], PromptForCredentials method [Windows Update Agent],IWebProxy interface, wua.iwebproxy_promptforcredentials, wuapi/IWebProxy::PromptForCredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWebProxy.PromptForCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebProxy::PromptForCredentials


## -description


Prompts the user for the password to use for proxy authentication.


## -parameters




### -param parentWindow [in]

The parent window of the dialog box in which the user enters the credentials.


### -param title [in]

The title to use for the dialog box in which the user enters the credentials.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



This method can be changed only by a user on the computer. This method can be accessed through the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface.

If null is specified for the parent window (for example, if you specified Nothing in Visual Basic), the dialog box is displayed on the desktop.




## -see-also




<a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>
 

 

