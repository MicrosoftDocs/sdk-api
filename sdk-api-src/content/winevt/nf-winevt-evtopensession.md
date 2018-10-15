---
UID: NF:winevt.EvtOpenSession
title: EvtOpenSession function
author: windows-sdk-content
description: Establishes a connection to a remote computer that you can use when calling the other Windows Event Log functions.
old-location: wes\evtopensession.htm
tech.root: wes
ms.assetid: 26f1745c-dcca-4452-872e-1fffe20f049c
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: EvtOpenSession, EvtOpenSession function [EventLog], wes.evtopensession, winevt/EvtOpenSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winevt.h
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtOpenSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtOpenSession function


## -description


Establishes a connection to a remote computer that you can use when calling the other Windows Event Log functions.


## -parameters




### -param LoginClass [in]

The connection method to use to connect to the remote computer. For possible values, see the <a href="https://msdn.microsoft.com/8d53402b-2d2c-4f93-8e98-4449701052b0">EVT_LOGIN_CLASS</a> enumeration.


### -param Login [in]

A <a href="https://msdn.microsoft.com/38f74619-1643-461f-b04b-c15567c06ca8">EVT_RPC_LOGIN</a> structure that identifies the remote computer that you want to connect to, the user's credentials, and the type of authentication to use when connecting.


### -param Timeout [in]

Reserved. Must be zero.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a session handle that you can use to access event log information on the remote computer; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



When you are finished with the session handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function. Closing the session handle will also close all open handles created in the session (closing the open handles cancels any current activity on those handles).

To connect to the remote computer, the remote computer must enable the "Remote Event Log Management" Windows Firewall exception; otherwise, when you try to use the session handle, the call will error with RPC_S_SERVER_UNAVAILABLE. The computer to which you are connecting must be running Windows Vista or later.

This function does not validate the credentials; the credentials are validated the first time you try to use the session handle. If the credentials are not valid, the call will fail with ERROR_ACCESS_DENIED.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/df789981-0e1c-4d68-9bd5-5d054f1724d4">Accessing Remote Computers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8d53402b-2d2c-4f93-8e98-4449701052b0">EVT_LOGIN_CLASS</a>



<a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a>
 

 

