---
UID: NF:userenv.RegisterGPNotification
title: RegisterGPNotification function
author: windows-sdk-content
description: The RegisterGPNotification function enables an application to receive notification when there is a change in policy. When a policy change occurs, the specified event object is set to the signaled state.
old-location: policy\registergpnotification.htm
old-project: Policy
ms.assetid: 0a758da3-73a8-4d9b-8663-e6cab1a1bd3f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: RegisterGPNotification, RegisterGPNotification function [Group Policy], _win32_registergpnotification, policy.registergpnotification, userenv/RegisterGPNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: userenv.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RegisterGPNotification
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# RegisterGPNotification function


## -description


The
    <b>RegisterGPNotification</b> function enables an application to receive notification when there is a change in policy. When a policy change occurs, the specified event object is set to the signaled state.


## -parameters




### -param hEvent [in]

Handle to an event object. Use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function to create the event object.


### -param bMachine [in]

Specifies the policy change type. If <b>TRUE</b>, computer policy changes are reported. If <b>FALSE</b>, user policy changes are reported.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/39ac1361-0160-44e3-8b99-ff50978cc425">UnregisterGPNotification</a> function to unregister the handle from receiving policy change notifications. Call the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle when it is no longer required.

An application can also receive notifications about policy changes when a 
<a href="https://msdn.microsoft.com/77174e06-a25b-440a-9e9c-4fd5979c433c">WM_SETTINGCHANGE</a> message is broadcast. In this instance, the <i>wParam</i> parameter value is 1 if computer policy was applied; it is zero if user policy was applied. The <i>lParam</i> parameter points to the string "Policy".




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/39ac1361-0160-44e3-8b99-ff50978cc425">UnregisterGPNotification</a>
 

 

