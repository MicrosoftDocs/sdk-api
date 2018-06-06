---
UID: NC:webapplication.UnregisterAuthoringClientFunctionType
title: UnregisterAuthoringClientFunctionType
author: windows-sdk-content
description: Unregisters the application-defined function that was registered with the RegisterAuthoringClientFunctionType function. This function is called when the app host terminates.
old-location: debug\unregisterauthoringclientfunctiontype.htm
old-project: debug_wwahost
ms.assetid: 2F48142B-88D2-49B7-9FAA-5D6BA4DC3837
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: UnregisterAuthoringClientFunctionType, UnregisterAuthoringClientFunctionType function, UnregisterAuthoringClientFunctionType function pointer [Debugging Windows Store apps], debug.unregisterauthoringclientfunctiontype, webapplication/UnregisterAuthoringClientFunctionType
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - webapplication.h
api_name:
 - UnregisterAuthoringClientFunctionType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# UnregisterAuthoringClientFunctionType callback function


## -description


Unregisters the application-defined function that was registered with the <a href="https://msdn.microsoft.com/31414CBA-12A3-45F8-967B-7ECD9D90D0F6">RegisterAuthoringClientFunctionType</a> function. This function is called when the app host  terminates.


## -parameters




### -param *host [in]

Type: <b><a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>*</b>

An object that provides a path to the authoring binary.


## -returns



Type: <b>HRESULT</b>

The WWAHost.




## -see-also




<a href="https://msdn.microsoft.com/31414CBA-12A3-45F8-967B-7ECD9D90D0F6">RegisterAuthoringClientFunctionType</a>
 

 

