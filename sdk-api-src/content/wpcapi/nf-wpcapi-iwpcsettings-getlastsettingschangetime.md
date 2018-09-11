---
UID: NF:wpcapi.IWPCSettings.GetLastSettingsChangeTime
title: IWPCSettings::GetLastSettingsChangeTime
author: windows-sdk-content
description: Retrieves the time at which the configuration settings were last updated.
old-location: parcon\iwpcsettings_getlastsettingschangetime.htm
tech.root: parcon
ms.assetid: 6fe5be0c-e6fa-481d-a28d-c5b15257b901
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetLastSettingsChangeTime, GetLastSettingsChangeTime method, GetLastSettingsChangeTime method,IWPCSettings interface, IWPCSettings interface,GetLastSettingsChangeTime method, IWPCSettings.GetLastSettingsChangeTime, IWPCSettings::GetLastSettingsChangeTime, parcon.iwpcsettings_getlastsettingschangetime, wpcapi/IWPCSettings::GetLastSettingsChangeTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCSettings.GetLastSettingsChangeTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWPCSettings::GetLastSettingsChangeTime


## -description


Retrieves the time at which the configuration settings were last updated.


## -parameters




### -param pTime [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the time at which the settings were last updated.


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




<a href="https://msdn.microsoft.com/92ae8611-fbb4-470e-8a48-395defaef904">IWPCSettings</a>
 

 

