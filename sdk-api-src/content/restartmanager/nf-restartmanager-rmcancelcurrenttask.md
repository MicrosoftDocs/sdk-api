---
UID: NF:restartmanager.RmCancelCurrentTask
title: RmCancelCurrentTask function
author: windows-sdk-content
description: Cancels the current RmShutdown or RmRestart operation. This function must be called from the application that has started the session by calling the RmStartSession function.
old-location: rstmgr\rmcancelcurrenttask.htm
tech.root: rstmgr
ms.assetid: 58a9a734-667a-48b0-84e2-8cfd85e918bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RmCancelCurrentTask, RmCancelCurrentTask function [Restart Mgr], restartmanager/RmCancelCurrentTask, rstmgr.rmcancelcurrenttask
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
 - RmCancelCurrentTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RmCancelCurrentTask function


## -description


Cancels the current  <a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a> or  <a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a> operation.  This function must be called from the application that has started the session by calling the <a href="https://msdn.microsoft.com/bc79c6e5-49e6-44d3-90f6-b0109fb9611b">RmStartSession</a> function. 


## -parameters




### -param dwSessionHandle [in]

A handle to an existing session.


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
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A cancellation of the current operation is requested.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a>



<a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a>
 

 

