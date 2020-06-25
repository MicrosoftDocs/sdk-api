---
UID: NF:authz.AuthzRegisterCapChangeNotification
title: AuthzRegisterCapChangeNotification function (authz.h)
description: Registers a CAP update notification callback.
helpviewer_keywords: ["AuthzRegisterCapChangeNotification","AuthzRegisterCapChangeNotification function [Security]","authz/AuthzRegisterCapChangeNotification","security.authzregistercapchangenotification"]
old-location: security\authzregistercapchangenotification.htm
tech.root: SecAuthZ
ms.assetid: B0675BB3-62FA-462E-8DFB-55C47576DFEC
ms.date: 12/05/2018
ms.keywords: AuthzRegisterCapChangeNotification, AuthzRegisterCapChangeNotification function [Security], authz/AuthzRegisterCapChangeNotification, security.authzregistercapchangenotification
f1_keywords:
- authz/AuthzRegisterCapChangeNotification
dev_langs:
- c++
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
- AuthzRegisterCapChangeNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuthzRegisterCapChangeNotification function


## -description


The <b>AuthzRegisterCapChangeNotification</b> function registers a CAP update notification callback.


## -parameters




### -param phCapChangeSubscription [out]

Pointer to the CAP change notification subscription handle. When you have finished using the handle, unsubscribe by passing this parameter to the <a href="https://docs.microsoft.com/windows/desktop/api/authz/nf-authz-authzunregistercapchangenotification">AuthzUnregisterCapChangeNotification</a> function.


### -param pfnCapChangeCallback [in]

The CAP change notification callback function.


### -param pCallbackContext [in, optional]

The context of the user to be passed to the callback function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function is intended for applications that manually manage CAP usage to get notified of CAP changes in the system. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/authz/nf-authz-authzunregistercapchangenotification">AuthzUnregisterCapChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/central-authorization-policies">Central Access Policies</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>
 

 

