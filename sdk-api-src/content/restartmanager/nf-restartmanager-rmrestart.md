---
UID: NF:restartmanager.RmRestart
title: RmRestart function (restartmanager.h)
author: windows-sdk-content
description: Restarts applications and services that have been shut down by the RmShutdown function and that have been registered to be restarted using the RegisterApplicationRestart function.
old-location: rstmgr\rmrestart.htm
tech.root: rstmgr
ms.assetid: e0939b31-0233-40d2-96cf-bbabe9488a12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RmRestart, RmRestart function [Restart Mgr], restartmanager/RmRestart, rstmgr.rmrestart
ms.topic: function
req.header: restartmanager.h
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
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rstrtmgr.dll
api_name:
 - RmRestart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RmRestart function


## -description


Restarts applications and services that have been shut down by the <a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a> function and that have been registered to be restarted using the <a href="https://msdn.microsoft.com/f4cd25b3-2aee-460f-9f9f-b45ecded094f">RegisterApplicationRestart</a> function. This function can only be called by the primary installer that called the <a href="https://msdn.microsoft.com/bc79c6e5-49e6-44d3-90f6-b0109fb9611b">RmStartSession</a> function to start the Restart Manager session.


## -parameters




### -param dwSessionHandle [in]

A handle to the existing Restart Manager session.


### -param dwRestartFlags

Reserved. This parameter should be 0.


### -param fnStatus [in, optional]

A pointer to a status message callback function that is used to communicate status while the <b>RmRestart</b> function is running. If <b>NULL</b>, no status is provided.


## -returns



This is the most recent error received. The function can return one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> that are defined in Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REQUEST_OUT_OF_SEQUENCE</b></dt>
<dt>776</dt>
</dl>
</td>
<td width="60%">
This error value is returned if the <a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a> function is called with a valid session handle before calling the <a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FAIL_RESTART</b></dt>
<dt>352</dt>
</dl>
</td>
<td width="60%">
One or more applications could not be restarted. The <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structures that are returned by the <a href="https://msdn.microsoft.com/de4feea4-2b45-4430-a4b3-8ca26c455e42">RmGetList</a> function contain updated status information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
<dt>121</dt>
</dl>
</td>
<td width="60%">
A Restart Manager function could not obtain a registry write mutex in the allotted time. A system restart is recommended because further use of the Restart Manager is likely to fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
<dt>1223</dt>
</dl>
</td>
<td width="60%">
This error value is returned by the <a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a> function when the request to cancel an operation is successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
An operation was unable  to read or write to the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
A Restart Manager operation could not complete because not enough memory was available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
No Restart Manager session exists for the handle supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The function succeeds and returns.

</td>
</tr>
</table>
 




## -remarks



After calling the <b>RmRestart</b> function, the <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structures that are returned by the <a href="https://msdn.microsoft.com/de4feea4-2b45-4430-a4b3-8ca26c455e42">RmGetList</a> function contain updated status information.  

The Restart Manager respects the privileges that separate different user or terminal sessions. An installer that is running as a service with LocalSystem privileges cannot shut down or restart any applications in another user or terminal session.  Installers should implement custom methods to shut down and restart applications that are running in other sessions. One method would be to start a new   installer process  in the other session to perform shutdown and restart operations.

When a console application is shut down and restarted by Restart Manager, the application is restarted in a new console.

Installers should always restart application and services using the <b>RmRestart</b> function even when the <a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a> function returns an error indicating that not all applications and services could be shut down.

The <b>RmRestart</b> function does not restart any applications that run with elevated privileges. Even if the application was shutdown by Restart Manager. 


 The <b>RmRestart</b> function does not restart any applications that do not run as the currently-logged on user. Even if the application was shutdown by Restart Manager. For example, the <b>RmRestart</b> function does not restart applications started with the <b>Run As</b> command that do not run as the currently-logged on user. These applications must be manually restarted. 




## -see-also




<a href="https://msdn.microsoft.com/f4cd25b3-2aee-460f-9f9f-b45ecded094f">RegisterApplicationRestart</a>



<a href="https://msdn.microsoft.com/58a9a734-667a-48b0-84e2-8cfd85e918bf">RmCancelCurrentTask</a>



<a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a>
 

 

