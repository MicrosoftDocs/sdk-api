---
UID: NF:wscapi.WscUnRegisterChanges
title: WscUnRegisterChanges function
author: windows-sdk-content
description: Cancels a callback registration that was made by a call to the WscRegisterForChanges function.
old-location: winprog\wscunregisterchanges.htm
old-project: DevNotes
ms.assetid: cfb0d076-bd8b-4483-a036-51c77b8181c9
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: WscUnRegisterChanges, WscUnRegisterChanges function [Windows API], winprog.wscunregisterchanges, wscapi/WscUnRegisterChanges
ms.prod: windows
ms.technology: windows-sdk
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
-	WscUnRegisterChanges
product: Windows
targetos: Windows
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WscUnRegisterChanges function


## -description


Cancels a callback registration that was made by a call to the <a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a> function.


## -parameters




### -param hRegistrationHandle [in]

The handle to the registration context returned as the <i>phCallbackRegistration</i> of the <a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a> function.


## -returns



Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a>
 

 

