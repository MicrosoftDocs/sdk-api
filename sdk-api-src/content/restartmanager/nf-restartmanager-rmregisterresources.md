---
UID: NF:restartmanager.RmRegisterResources
title: RmRegisterResources function
author: windows-sdk-content
description: Registers resources to a Restart Manager session.
old-location: rstmgr\rmregisterresources.htm
tech.root: RstMgr
ms.assetid: 9ac94461-bf75-4517-b47e-23d82474efe8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RmRegisterResources, RmRegisterResources function [Restart Mgr], restartmanager/RmRegisterResources, rstmgr.rmregisterresources
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RmRegisterResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RmRegisterResources function


## -description


Registers resources to a Restart Manager session. The Restart Manager uses the list of resources registered with the session to determine which applications and services must be shut down and restarted. Resources can be identified by filenames, service short names, or <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structures that describe running applications. The <b>RmRegisterResources</b> function can be used by a primary or secondary installer.


## -parameters




### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.


### -param nFiles [in]

The number of files being registered.


### -param rgsFileNames [in, optional]

An array of <b>null</b>-terminated strings of full filename paths. This parameter can be <b>NULL</b> if <i>nFiles</i> is 0.


### -param nApplications [in]

The number of processes being registered.


### -param rgApplications [in, optional]

An array of <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structures. This parameter can be <b>NULL</b> if <i>nApplications</i> is 0.


### -param nServices [in]

The number of services to be registered.


### -param rgsServiceNames [in, optional]

An array of <b>null</b>-terminated strings of service short names. This parameter can be <b>NULL</b> if <i>nServices</i> is 0.


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
The resources specified have been registered.

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
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by Restart Manager function if a <b>NULL</b> pointer or 0 is passed in a parameter that requires a non-<b>null</b> and non-zero value.

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
</table>
 




## -remarks



Each call to the <b>RmRegisterResources</b> function performs relatively expensive write operations. Do not call this function once per file, instead group related files together into components and register these together.



