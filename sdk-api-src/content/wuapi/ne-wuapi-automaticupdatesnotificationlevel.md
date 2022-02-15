---
UID: NE:wuapi.tagAutomaticUpdatesNotificationLevel
title: AutomaticUpdatesNotificationLevel (wuapi.h)
description: Defines the possible ways in which elevated users are notified about Automatic Updates events.
helpviewer_keywords: ["AutomaticUpdatesNotificationLevel","AutomaticUpdatesNotificationLevel enumeration [Windows Update Agent]","aunlDisabled","aunlNotConfigured","aunlNotifyBeforeDownload","aunlNotifyBeforeInstallation","aunlScheduledInstallation","wua.automaticupdatesnotificationlevel","wuapi/AutomaticUpdatesNotificationLevel","wuapi/aunlDisabled","wuapi/aunlNotConfigured","wuapi/aunlNotifyBeforeDownload","wuapi/aunlNotifyBeforeInstallation","wuapi/aunlScheduledInstallation"]
old-location: wua\automaticupdatesnotificationlevel.htm
tech.root: wua
ms.assetid: a326400b-d6df-4947-8ab8-126d357834c3
ms.date: 12/05/2018
ms.keywords: AutomaticUpdatesNotificationLevel, AutomaticUpdatesNotificationLevel enumeration [Windows Update Agent], aunlDisabled, aunlNotConfigured, aunlNotifyBeforeDownload, aunlNotifyBeforeInstallation, aunlScheduledInstallation, wua.automaticupdatesnotificationlevel, wuapi/AutomaticUpdatesNotificationLevel, wuapi/aunlDisabled, wuapi/aunlNotConfigured, wuapi/aunlNotifyBeforeDownload, wuapi/aunlNotifyBeforeInstallation, wuapi/aunlScheduledInstallation
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AutomaticUpdatesNotificationLevel
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAutomaticUpdatesNotificationLevel
 - wuapi/tagAutomaticUpdatesNotificationLevel
 - AutomaticUpdatesNotificationLevel
 - wuapi/AutomaticUpdatesNotificationLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - AutomaticUpdatesNotificationLevel
---

# AutomaticUpdatesNotificationLevel enumeration


## -description

Defines the possible ways in which elevated users are notified about   Automatic Updates events.

## -enum-fields

### -field aunlNotConfigured:0

Automatic Updates is not configured by the user or by a Group Policy administrator. Users are periodically prompted to configure Automatic Updates.

### -field aunlDisabled:1

Automatic Updates is disabled. Users are not  notified of important updates for the computer.

### -field aunlNotifyBeforeDownload:2

Automatic Updates  prompts users to approve updates before it downloads or installs the updates.

### -field aunlNotifyBeforeInstallation:3

Automatic Updates  automatically downloads updates, but  prompts users to approve the updates before installation.

### -field aunlScheduledInstallation:4

Automatic Updates  automatically installs updates according to the schedule that is specified by the user or by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday">IAutomaticUpdatesSettings.ScheduledInstallationDay</a> and <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">IAutomaticUPdatesSettings.ScheduledInstallationTime</a> properties. This setting is the recommended setting.
