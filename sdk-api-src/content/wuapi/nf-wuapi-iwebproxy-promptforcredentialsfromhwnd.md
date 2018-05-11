---
UID: NF:wuapi.IWebProxy.PromptForCredentialsFromHwnd
title: IWebProxy::PromptForCredentialsFromHwnd
author: windows-driver-content
description: Prompts the user for a password to use for proxy authentication using the hWnd property of the parent window.
old-location: wua\iwebproxy_promptforcredentialsfromhwnd.htm
old-project: Wua_Sdk
ms.assetid: 36ee1771-cfa6-4fa0-924b-69dbd57b1ad4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWebProxy interface [Windows Update Agent],PromptForCredentialsFromHwnd method, IWebProxy.PromptForCredentialsFromHwnd, IWebProxy::PromptForCredentialsFromHwnd, PromptForCredentialsFromHwnd, PromptForCredentialsFromHwnd method [Windows Update Agent], PromptForCredentialsFromHwnd method [Windows Update Agent],IWebProxy interface, wua.iwebproxy_promptforcredentialsfromhwnd, wuapi/IWebProxy::PromptForCredentialsFromHwnd
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IWebProxy.PromptForCredentialsFromHwnd
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWebProxy::PromptForCredentialsFromHwnd


## -description


Prompts the user for a password to use for proxy authentication using the <b>hWnd</b> property of the parent window.


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
 

 

