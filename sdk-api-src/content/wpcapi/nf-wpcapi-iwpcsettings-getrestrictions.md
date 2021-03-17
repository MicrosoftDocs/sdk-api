---
UID: NF:wpcapi.IWPCSettings.GetRestrictions
title: IWPCSettings::GetRestrictions (wpcapi.h)
description: Determines whether web restrictions, time limits, or game restrictions are on.
helpviewer_keywords: ["GetRestrictions","GetRestrictions method","GetRestrictions method","IWPCSettings interface","IWPCSettings interface","GetRestrictions method","IWPCSettings.GetRestrictions","IWPCSettings::GetRestrictions","WPCFLAG_APPS_RESTRICTED","WPCFLAG_GAMES_BLOCKED","WPCFLAG_HOURS_RESTRICTED","WPCFLAG_LOGGING_REQUIRED","WPCFLAG_NO_RESTRICTION","WPCFLAG_WEB_FILTERED","parcon.iwpcsettings_getrestrictions","wpcapi/IWPCSettings::GetRestrictions"]
old-location: parcon\iwpcsettings_getrestrictions.htm
tech.root: parcon
ms.assetid: 22350ef3-3068-4d33-a023-74644e5fbb83
ms.date: 12/05/2018
ms.keywords: GetRestrictions, GetRestrictions method, GetRestrictions method,IWPCSettings interface, IWPCSettings interface,GetRestrictions method, IWPCSettings.GetRestrictions, IWPCSettings::GetRestrictions, WPCFLAG_APPS_RESTRICTED, WPCFLAG_GAMES_BLOCKED, WPCFLAG_HOURS_RESTRICTED, WPCFLAG_LOGGING_REQUIRED, WPCFLAG_NO_RESTRICTION, WPCFLAG_WEB_FILTERED, parcon.iwpcsettings_getrestrictions, wpcapi/IWPCSettings::GetRestrictions
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWPCSettings::GetRestrictions
 - wpcapi/IWPCSettings::GetRestrictions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCSettings.GetRestrictions
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

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcsettings">IWPCSettings</a>