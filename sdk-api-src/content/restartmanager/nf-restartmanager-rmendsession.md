---
UID: NF:restartmanager.RmEndSession
title: RmEndSession function
author: windows-sdk-content
description: Ends the Restart Manager session.
old-location: rstmgr\rmendsession.htm
old-project: RstMgr
ms.assetid: 2681cb69-a66f-4aec-a164-98d2d28f9908
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RmEndSession, RmEndSession function [Restart Mgr], restartmanager/RmEndSession, rstmgr.rmendsession
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RM_SHUTDOWN_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rstrtmgr.dll
api_name:
 - RmEndSession
product: Windows
targetos: Windows
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
req.product: ADAM
---

# RmEndSession function


## -description


Ends the Restart Manager session. This function should be called by the primary installer that has previously started the session by calling the <a href="https://msdn.microsoft.com/bc79c6e5-49e6-44d3-90f6-b0109fb9611b">RmStartSession</a> function. The <b>RmEndSession</b> function can be called by a secondary installer that is joined to the session once no more resources need to be registered by the secondary installer.   


## -parameters




### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.


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
The function completed successfully.

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
A Restart Manager function could not obtain a Registry write mutex in the allotted time. A system restart is recommended because further use of the Restart Manager is likely to fail.

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
An invalid handle was passed to the function. No Restart Manager session exists for the handle supplied.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f9cb2d81-a2bc-4bb7-920a-1630354ea942">RmJoinSession</a>



<a href="https://msdn.microsoft.com/bc79c6e5-49e6-44d3-90f6-b0109fb9611b">RmStartSession</a>
 

 

