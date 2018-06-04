---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

