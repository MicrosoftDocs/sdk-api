---
UID: NF:authz.AuthzUnregisterCapChangeNotification
title: AuthzUnregisterCapChangeNotification function
author: windows-sdk-content
description: Removes a previously registered CAP update notification callback.
old-location: security\authzunregistercapchangenotification.htm
tech.root: secauthz
ms.assetid: 79374C66-CD50-4351-A16B-AF79A579AF74
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AuthzUnregisterCapChangeNotification, AuthzUnregisterCapChangeNotification function [Security], authz/AuthzUnregisterCapChangeNotification, security.authzunregistercapchangenotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: authz.h
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzUnregisterCapChangeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AuthzUnregisterCapChangeNotification function


## -description


The <b>AuthzUnregisterCapChangeNotification</b> function removes a previously registered CAP update notification callback.


## -parameters




### -param hCapChangeSubscription [in]

Handle of the CAP change notification subscription to unregister.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function blocks operations until all callbacks are complete. Do not call this function from inside a callback function because it will cause a deadlock. 




## -see-also




<a href="https://msdn.microsoft.com/B0675BB3-62FA-462E-8DFB-55C47576DFEC">AuthzRegisterCapChangeNotification</a>



<a href="https://msdn.microsoft.com/E3E43D9F-6826-468A-86E9-AC8F9A381FD4">Central Access Policies</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>
 

 

