---
UID: NF:wuapi.IAutomaticUpdatesSettings.put_ScheduledInstallationDay
title: IAutomaticUpdatesSettings::put_ScheduledInstallationDay (wuapi.h)
description: Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates. (Put)
helpviewer_keywords: ["IAutomaticUpdatesSettings interface [Windows Update Agent]","ScheduledInstallationDay property","IAutomaticUpdatesSettings.ScheduledInstallationDay","IAutomaticUpdatesSettings.put_ScheduledInstallationDay","IAutomaticUpdatesSettings::ScheduledInstallationDay","IAutomaticUpdatesSettings::get_ScheduledInstallationDay","IAutomaticUpdatesSettings::put_ScheduledInstallationDay","ScheduledInstallationDay property [Windows Update Agent]","ScheduledInstallationDay property [Windows Update Agent]","IAutomaticUpdatesSettings interface","put_ScheduledInstallationDay","wua.iautomaticupdatessettings_scheduledinstallationday","wuapi/IAutomaticUpdatesSettings::ScheduledInstallationDay","wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationDay","wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationDay"]
old-location: wua\iautomaticupdatessettings_scheduledinstallationday.htm
tech.root: wua
ms.assetid: 057498ad-d329-4fda-b3fe-95bdc27d62a4
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],ScheduledInstallationDay property, IAutomaticUpdatesSettings.ScheduledInstallationDay, IAutomaticUpdatesSettings.put_ScheduledInstallationDay, IAutomaticUpdatesSettings::ScheduledInstallationDay, IAutomaticUpdatesSettings::get_ScheduledInstallationDay, IAutomaticUpdatesSettings::put_ScheduledInstallationDay, ScheduledInstallationDay property [Windows Update Agent], ScheduledInstallationDay property [Windows Update Agent],IAutomaticUpdatesSettings interface, put_ScheduledInstallationDay, wua.iautomaticupdatessettings_scheduledinstallationday, wuapi/IAutomaticUpdatesSettings::ScheduledInstallationDay, wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationDay, wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationDay
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutomaticUpdatesSettings::put_ScheduledInstallationDay
 - wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationDay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings.ScheduledInstallationDay
 - IAutomaticUpdatesSettings.get_ScheduledInstallationDay
 - IAutomaticUpdatesSettings.put_ScheduledInstallationDay
---

# IAutomaticUpdatesSettings::put_ScheduledInstallationDay


## -description

<p class="CCE_Message">[<b>IAutomaticUpdatesSettings::ScheduledInstallationDay</b> is no longer supported as of Windows 10.]


Gets and sets the days of the week on which Automatic Updates  installs or uninstalls updates.



This property is read/write.

## -parameters

## -remarks

The value of this property is ignored if the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> property is not <b>aunlScheduledInstallation</b>.

<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <b>ScheduledInstallationDay</b> is not supported and will return unreliable values. If you try to modify <b>ScheduledInstallationDay</b>, the operation will appear to succeed but will have no effect.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
