---
UID: NF:userenv.UnregisterGPNotification
title: UnregisterGPNotification function
author: windows-sdk-content
description: The UnregisterGPNotification function unregisters the specified policy-notification handle from receiving policy change notifications.
old-location: policy\unregistergpnotification.htm
tech.root: Policy
ms.assetid: 39ac1361-0160-44e3-8b99-ff50978cc425
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UnregisterGPNotification, UnregisterGPNotification function [Group Policy], _win32_unregistergpnotification, policy.unregistergpnotification, userenv/UnregisterGPNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - UnregisterGPNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnregisterGPNotification function


## -description


The 
    <b>UnregisterGPNotification</b> function unregisters the specified policy-notification handle from receiving policy change notifications.


## -parameters




### -param hEvent [in]

Policy-notification handle passed to the 
<a href="https://msdn.microsoft.com/0a758da3-73a8-4d9b-8663-e6cab1a1bd3f">RegisterGPNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller must call the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/0a758da3-73a8-4d9b-8663-e6cab1a1bd3f">RegisterGPNotification</a>
 

 

