---
UID: NF:wuapi.IAutomaticUpdates.ShowSettingsDialog
title: IAutomaticUpdates::ShowSettingsDialog (wuapi.h)
description: Displays a dialog box that contains settings for Automatic Updates.helpviewer_keywords: ["IAutomaticUpdates interface [Windows Update Agent]","ShowSettingsDialog method","IAutomaticUpdates.ShowSettingsDialog","IAutomaticUpdates::ShowSettingsDialog","ShowSettingsDialog","ShowSettingsDialog method [Windows Update Agent]","ShowSettingsDialog method [Windows Update Agent]","IAutomaticUpdates interface","wua.iautomaticupdates_showsettingsdialog","wuapi/IAutomaticUpdates::ShowSettingsDialog"]
old-location: wua\iautomaticupdates_showsettingsdialog.htm
tech.root: Wua_Sdk
ms.assetid: da153799-9414-4e8e-aed4-96e0fff9ca88
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdates interface [Windows Update Agent],ShowSettingsDialog method, IAutomaticUpdates.ShowSettingsDialog, IAutomaticUpdates::ShowSettingsDialog, ShowSettingsDialog, ShowSettingsDialog method [Windows Update Agent], ShowSettingsDialog method [Windows Update Agent],IAutomaticUpdates interface, wua.iautomaticupdates_showsettingsdialog, wuapi/IAutomaticUpdates::ShowSettingsDialog
f1_keywords:
- wuapi/IAutomaticUpdates.ShowSettingsDialog
dev_langs:
- c++
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IAutomaticUpdates.ShowSettingsDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutomaticUpdates::ShowSettingsDialog


## -description


<p class="CCE_Message">[<b>IAutomaticUpdates::ShowSettingsDialog</b> is no longer supported. Starting with 
    Windows 10 calls to <b>ShowSettingsDialog</b> always return 
    <b>S_OK</b>, but do nothing.]

Displays a dialog box that contains settings for Automatic Updates.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the following conditions are true:

<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is set to <a href="https://docs.microsoft.com/windows/desktop/api/wuapicommon/ne-wuapicommon-serverselection">ssManagedServer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapicommon/ne-wuapicommon-serverselection">ssDefault</a>.</li>
<li>The managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



A call to <b>ShowSettingsDialog</b>  fails if the calling user is not logged on or does not have a desktop.
A caller can also programmatically modify Automatic Updates settings by using the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-get_settings">Settings</a> property.

The settings in the dialog box are read-only if the caller has insufficient security permissions or if the settings are enforced by a domain administrator who is using Group Policy settings.

 This method returns <b>WU_E_AU_NOSERVICE</b> if Automatic Updates is disabled, initializing, uninitializing, or not configured.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">IAutomaticUpdates</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-get_settings">IAutomaticUpdates.Settings</a>
 

 

