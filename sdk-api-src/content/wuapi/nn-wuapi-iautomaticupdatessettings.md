---
UID: NN:wuapi.IAutomaticUpdatesSettings
title: IAutomaticUpdatesSettings (wuapi.h)

description: Contains the settings that are available in Automatic Updates.
old-location: wua\iautomaticupdatessettings.htm
tech.root: Wua_Sdk
ms.assetid: c4672df5-9e47-45f5-9504-1ebb0bf3c6a6

ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings, IAutomaticUpdatesSettings interface [Windows Update Agent], IAutomaticUpdatesSettings interface [Windows Update Agent],described, wua.iautomaticupdatessettings, wuapi/IAutomaticUpdatesSettings
ms.topic: interface
f1_keywords: 
 - "wuapi/IAutomaticUpdatesSettings"
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
 - IAutomaticUpdatesSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutomaticUpdatesSettings interface


## -description


 Contains the settings that are available in Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAutomaticUpdatesSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAutomaticUpdatesSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Retrieves the latest Automatic Updates settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">Save</a>
</td>
<td align="left" width="63%">
Applies the current Automatic Updates settings.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets how elevated users are notified of Automatic Updates events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the Automatic Update settings are read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_required">Required</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether Group Policy  requires the Automatic Updates service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday">ScheduledInstallationDay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the days of the week on which Automatic Updates  installs or uninstalls updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">ScheduledInstallationTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the time at which Automatic Updates  installs or uninstalls updates.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday">ScheduledInstallationDay</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">ScheduledInstallationTime</a> are not supported and will return unreliable values. If you try to modify these properties, the operation will appear to succeed but will have no effect.</div>
<div> </div>
<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">IAutomaticUpdatesSettings::Save</a> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">aunlScheduledInstallation</a>).</div>
<div> </div>


