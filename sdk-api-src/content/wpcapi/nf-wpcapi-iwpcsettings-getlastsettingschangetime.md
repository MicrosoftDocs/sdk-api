---
UID: NF:wpcapi.IWPCSettings.GetLastSettingsChangeTime
title: IWPCSettings::GetLastSettingsChangeTime (wpcapi.h)
description: Retrieves the time at which the configuration settings were last updated.
helpviewer_keywords: ["GetLastSettingsChangeTime","GetLastSettingsChangeTime method","GetLastSettingsChangeTime method","IWPCSettings interface","IWPCSettings interface","GetLastSettingsChangeTime method","IWPCSettings.GetLastSettingsChangeTime","IWPCSettings::GetLastSettingsChangeTime","parcon.iwpcsettings_getlastsettingschangetime","wpcapi/IWPCSettings::GetLastSettingsChangeTime"]
old-location: parcon\iwpcsettings_getlastsettingschangetime.htm
tech.root: parcon
ms.assetid: 6fe5be0c-e6fa-481d-a28d-c5b15257b901
ms.date: 12/05/2018
ms.keywords: GetLastSettingsChangeTime, GetLastSettingsChangeTime method, GetLastSettingsChangeTime method,IWPCSettings interface, IWPCSettings interface,GetLastSettingsChangeTime method, IWPCSettings.GetLastSettingsChangeTime, IWPCSettings::GetLastSettingsChangeTime, parcon.iwpcsettings_getlastsettingschangetime, wpcapi/IWPCSettings::GetLastSettingsChangeTime
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
 - IWPCSettings::GetLastSettingsChangeTime
 - wpcapi/IWPCSettings::GetLastSettingsChangeTime
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
 - IWPCSettings.GetLastSettingsChangeTime
---

# IWPCSettings::GetLastSettingsChangeTime


## -description

Retrieves the time at which the configuration settings were last updated.

## -parameters

### -param pTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the time at which the settings were last updated.

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