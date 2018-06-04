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

# IWPCSettings::GetRestrictions


## -description


Determines whether web restrictions, time limits, or game restrictions are on.


## -parameters




### -param pdwRestrictions [out]

Indicates the current restrictions. This parameter can be one of more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_NO_RESTRICTION"></a><a id="wpcflag_no_restriction"></a><dl>
<dt><b>WPCFLAG_NO_RESTRICTION</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
There are no restrictions.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_LOGGING_REQUIRED"></a><a id="wpcflag_logging_required"></a><dl>
<dt><b>WPCFLAG_LOGGING_REQUIRED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Activity logged is on.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WEB_FILTERED"></a><a id="wpcflag_web_filtered"></a><dl>
<dt><b>WPCFLAG_WEB_FILTERED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
A Web Content Filter is active.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_HOURS_RESTRICTED"></a><a id="wpcflag_hours_restricted"></a><dl>
<dt><b>WPCFLAG_HOURS_RESTRICTED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Hours are restricted.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_GAMES_BLOCKED"></a><a id="wpcflag_games_blocked"></a><dl>
<dt><b>WPCFLAG_GAMES_BLOCKED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Games are blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_APPS_RESTRICTED"></a><a id="wpcflag_apps_restricted"></a><dl>
<dt><b>WPCFLAG_APPS_RESTRICTED</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Applications are restricted.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process has insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The user settings were not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/92ae8611-fbb4-470e-8a48-395defaef904">IWPCSettings</a>
 

 

