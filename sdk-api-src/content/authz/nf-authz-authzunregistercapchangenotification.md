---
UID: NF:authz.AuthzUnregisterCapChangeNotification
title: AuthzUnregisterCapChangeNotification function (authz.h)
description: Removes a previously registered CAP update notification callback.
old-location: security\authzunregistercapchangenotification.htm
tech.root: SecAuthZ
ms.assetid: 79374C66-CD50-4351-A16B-AF79A579AF74
ms.date: 12/05/2018
ms.keywords: AuthzUnregisterCapChangeNotification, AuthzUnregisterCapChangeNotification function [Security], authz/AuthzUnregisterCapChangeNotification, security.authzunregistercapchangenotification
f1_keywords:
- authz/AuthzUnregisterCapChangeNotification
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
- AuthzUnregisterCapChangeNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function blocks operations until all callbacks are complete. Do not call this function from inside a callback function because it will cause a deadlock. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/authz/nf-authz-authzregistercapchangenotification">AuthzRegisterCapChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/central-authorization-policies">Central Access Policies</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>
 

 

