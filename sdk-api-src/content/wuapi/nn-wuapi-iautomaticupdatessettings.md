---
UID: NN:wuapi.IAutomaticUpdatesSettings
title: IAutomaticUpdatesSettings
author: windows-sdk-content
description: Contains the settings that are available in Automatic Updates.
old-location: wua\iautomaticupdatessettings.htm
old-project: wua_sdk
ms.assetid: c4672df5-9e47-45f5-9504-1ebb0bf3c6a6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IAutomaticUpdatesSettings, IAutomaticUpdatesSettings interface [Windows Update Agent], IAutomaticUpdatesSettings interface [Windows Update Agent],described, wua.iautomaticupdatessettings, wuapi/IAutomaticUpdatesSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IAutomaticUpdatesSettings interface


## -description


 Contains the settings that are available in Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAutomaticUpdatesSettings</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/308426d9-d524-406a-931c-1fdb854aa4fb">Refresh</a>
</td>
<td align="left" width="63%">
Retrieves the latest Automatic Updates settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
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

<a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">NotificationLevel</a>


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

<a href="https://msdn.microsoft.com/e7a066b9-9581-4573-82e2-a6f2ca7440ac">ReadOnly</a>


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

<a href="https://msdn.microsoft.com/d3700208-4e87-495e-98cf-cc495b380528">Required</a>


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

<a href="https://msdn.microsoft.com/057498ad-d329-4fda-b3fe-95bdc27d62a4">ScheduledInstallationDay</a>


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

<a href="https://msdn.microsoft.com/1b1adefc-785e-46ad-8984-d2beb1c2202c">ScheduledInstallationTime</a>


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



<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <a href="https://msdn.microsoft.com/057498ad-d329-4fda-b3fe-95bdc27d62a4">ScheduledInstallationDay</a> and <a href="https://msdn.microsoft.com/1b1adefc-785e-46ad-8984-d2beb1c2202c">ScheduledInstallationTime</a> are not supported and will return unreliable values. If you try to modify these properties, the operation will appear to succeed but will have no effect.</div>
<div> </div>
<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <a href="https://msdn.microsoft.com/fb54b900-345a-4b36-b16d-52790c0266f6">IAutomaticUpdatesSettings::Save</a> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="automaticupdatesnotificationlevel.htm">aunlScheduledInstallation</a>).</div>
<div> </div>


