---
UID: NF:webapplication.IWebApplicationHost.Refresh
title: IWebApplicationHost::Refresh
author: windows-sdk-content
description: Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.
old-location: debug\iwebapplicationhost_refresh.htm
old-project: debug_wwahost
ms.assetid: 66f94cc9-9407-4844-a100-8144fc6f45ce
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWebApplicationHost interface [Debugging Windows Store apps],Refresh method, IWebApplicationHost.Refresh, IWebApplicationHost::Refresh, Refresh, Refresh method [Debugging Windows Store apps], Refresh method [Debugging Windows Store apps],IWebApplicationHost interface, debug.iwebapplicationhost_refresh, webapplication/IWebApplicationHost::Refresh
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
 - IWebApplicationHost.Refresh
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWebApplicationHost::Refresh


## -description


Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use this method when the currently executing code is outside of the activation path. If the code is executing inside the activation path, use <a href="https://msdn.microsoft.com/FBBA086D-1B20-4F70-B162-DD922DC5C4BF">IWebApplicationActivation::CancelPendingActivation</a> instead. 




## -see-also




<a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>
 

 

