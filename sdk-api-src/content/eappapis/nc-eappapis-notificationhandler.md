---
UID: NC:eappapis.NotificationHandler
title: NotificationHandler
author: windows-sdk-content
description: Notifies the supplicant that there is a change in the Statement of Health (SoH) and re-authentication of a Network Access Protection (NAP) system connection is required.
old-location: eaphost\notificationhandler.htm
tech.root: EAPHost
ms.assetid: 7fa12cb4-694a-4db6-9743-5a2cbb995721
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: NotificationHandler, NotificationHandler callback, NotificationHandler callback function [EAPHost], eaphost.notificationhandler, eappapis/NotificationHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eappapis.h
api_name:
 - NotificationHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NotificationHandler callback function


## -description


A callback prototype that notifies the supplicant that there is a change  in the Statement of Health (SoH) and re-authentication of a <a href="https://msdn.microsoft.com/f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e">Network Access Protection</a> (NAP) system connection is required. For the user to receive visual notification of a change in the SoH, the callback must remain in place until after authentication is complete.
<div class="alert"><b>Note</b>  Never cancel the callback while re-authentication is in progress and the network connection is still valid. Never attempt to use any other mechanism to notify the supplicant that the SoH has changed.  </div><div> </div>

## -parameters




### -param connectionId [in]

A GUID provided by the supplicant to EAPHost. This value specifies the logical network connection to re-authenticate.


### -param *pContextData [in]

Context data provided to EAPHost by the supplicant. This context data can be used by the supplicant for re-authentication.


## -returns



This callback function does not return a value.




## -remarks



A pointer to this callback function must be provided when calling <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>. The callback may be called by EAPHost at any time prior to calling <a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a>.




## -see-also




<a href="https://msdn.microsoft.com/a32ff75d-17c2-482f-b22d-0f6bf6003772">EAPHost Supplicant Callbacks</a>
 

 

