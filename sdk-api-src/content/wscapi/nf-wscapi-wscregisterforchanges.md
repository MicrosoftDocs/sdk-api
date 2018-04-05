---
UID: NF:wscapi.WscRegisterForChanges
title: WscRegisterForChanges function
author: windows-driver-content
description: Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.
old-location: winprog\wscregisterforchanges.htm
old-project: DevNotes
ms.assetid: 55f2d281-6308-4344-98dc-3b1c7cbee9df
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WscRegisterForChanges, WscRegisterForChanges function [Windows API], winprog.wscregisterforchanges, wscapi/WscRegisterForChanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSC_SECURITY_PROVIDER_HEALTH, *PWSC_SECURITY_PROVIDER_HEALTH
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wscapi.dll
api_name:
-	WscRegisterForChanges
product: Windows
targetos: Windows
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WscRegisterForChanges function


## -description


Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.


## -parameters




### -param Reserved [in]

Reserved.  Must be <b>NULL</b>.


### -param phCallbackRegistration [out]

A pointer to a handle to the callback registration. When you are finished using the callback function, unregister it by calling the <a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a> function.


### -param lpCallbackAddress [in]

A pointer to the application-defined function to be called when a change to the WSC service occurs. This function is also called when the WSC service is started or stopped.


### -param pContext [in]

A pointer to a variable to be passed as  the <i>lpParameter</i> parameter to the function pointed to by the <i>lpCallbackAddress</i> parameter.


## -returns



Returns S_OK if the function succeeds, otherwise returns an error code.




## -remarks



When you want to cease receiving notification to your callback method, you can unregister it by calling the <a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a> function.




## -see-also




<a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a>
 

 

