---
UID: NF:restartmanager.RmAddFilter
title: RmAddFilter function
author: windows-sdk-content
description: Modifies the shutdown or restart actions that are applied to an application or service.
old-location: rstmgr\rmaddfilter.htm
old-project: RstMgr
ms.assetid: 63d1d1d2-d7b7-4d6c-99f9-b849229e171f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RmAddFilter, RmAddFilter function [Restart Mgr], restartmanager/RmAddFilter, rstmgr.rmaddfilter
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
 - RmAddFilter
product: Windows
targetos: Windows
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
req.product: ADAM
---

# RmAddFilter function


## -description


Modifies the shutdown or restart actions that are applied to an application or service. The primary installer can call the <b>RmAddFilter</b> function multiple times. The most recent call overrides any previous modifications to the same file, process, or service.


## -parameters




### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.


### -param strModuleName

TBD


### -param pProcess

TBD


### -param strServiceShortName

TBD


### -param FilterAction

TBD




#### - ActionType [in]

An <a href="https://msdn.microsoft.com/68f77dbc-14cb-4b87-9589-328b1cef38d9">RM_FILTER_ACTION</a> enumeration value that specifies the type of modification to be applied.


#### - Application [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure for the application.  Modifications to shutdown or restart actions are applied for the application that is referenced by the <b>RM_UNIQUE_PROCESS</b> structure. This parameter must be <b>NULL</b> if the <i>strFilename</i>  or <i>strShortServiceName</i> parameter is non-<b>NULL</b>.


#### - strFilename [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the full path to the application's executable file. Modifications to shutdown or restart actions are applied for the application that is referenced by the full path.  This parameter must be <b>NULL</b> if the <i>Application</i> or <i>strServiceShortName</i> parameter is non-<b>NULL</b>.


#### - strShortServiceName [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the short service name. Modifications to shutdown or restart actions are applied for the service that is referenced by short service filename.  This parameter must be <b>NULL</b> if the <i>strFilename</i> or <i>Application</i> parameter is non-<b>NULL</b>.


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
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in as a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SESSION_CREDENTIAL_CONFLICT</b></dt>
<dt> 1219</dt>
</dl>
</td>
<td width="60%">
This error is returned when a secondary installer calls this function. This function is only available to primary installers.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a>
 

 

