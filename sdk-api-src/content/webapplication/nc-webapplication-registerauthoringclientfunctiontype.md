---
UID: NC:webapplication.RegisterAuthoringClientFunctionType
title: RegisterAuthoringClientFunctionType
author: windows-sdk-content
description: Defines a pointer to an application-defined function in a dynamic-link library (DLL) that will be used as the authoring binary. When the app host starts in authoring mode, this function is called to initialize the authoring binary.
old-location: debug\registerauthoringclientfunctiontype.htm
old-project: debug_wwahost
ms.assetid: 31414CBA-12A3-45F8-967B-7ECD9D90D0F6
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RegisterAuthoringClientFunctionType, RegisterAuthoringClientFunctionType function, RegisterAuthoringClientFunctionType function pointer [Debugging Windows Store apps], debug.registerauthoringclientfunctiontype, webapplication/RegisterAuthoringClientFunctionType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	webapplication.h
api_name:
-	RegisterAuthoringClientFunctionType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# RegisterAuthoringClientFunctionType callback function


## -description


Defines a pointer to an application-defined function in a dynamic-link library (DLL) that will be used as the authoring binary. When the app host starts in authoring mode, this function is called to initialize the authoring binary. 


## -parameters




### -param *authoringModeObject [in]

Type: <b><a href="https://msdn.microsoft.com/c33793c9-499e-4a57-b52d-345d3b360789">IWebApplicationAuthoringMode</a>*</b>

An object that provides a path to the authoring binary.


### -param *host [in]

Type: <b><a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>*</b>

The WWAHost. 


## -returns



Type: <b>HRESULT</b>

If this function pointer succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2F48142B-88D2-49B7-9FAA-5D6BA4DC3837">UnregisterAuthoringClientFunctionType</a>
 

 

