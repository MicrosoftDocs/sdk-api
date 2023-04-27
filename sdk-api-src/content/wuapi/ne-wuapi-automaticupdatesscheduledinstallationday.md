---
UID: NE:wuapi.tagAutomaticUpdatesScheduledInstallationDay
title: AutomaticUpdatesScheduledInstallationDay (wuapi.h)
description: Defines the days of the week when Automatic Updates installs or uninstalls updates.
helpviewer_keywords: ["AutomaticUpdatesScheduledInstallationDay","AutomaticUpdatesScheduledInstallationDay enumeration [Windows Update Agent]","ausidEveryDay","ausidEveryFriday","ausidEveryMonday","ausidEverySaturday","ausidEverySunday","ausidEveryThursday","ausidEveryTuesday","ausidEveryWednesday","wua.automaticupdatesscheduledinstallationday","wuapi/AutomaticUpdatesScheduledInstallationDay","wuapi/ausidEveryDay","wuapi/ausidEveryFriday","wuapi/ausidEveryMonday","wuapi/ausidEverySaturday","wuapi/ausidEverySunday","wuapi/ausidEveryThursday","wuapi/ausidEveryTuesday","wuapi/ausidEveryWednesday"]
old-location: wua\automaticupdatesscheduledinstallationday.htm
tech.root: wua
ms.assetid: 8c7525bf-e15f-4c30-8e16-4b945d73f3cb
ms.date: 12/05/2018
ms.keywords: AutomaticUpdatesScheduledInstallationDay, AutomaticUpdatesScheduledInstallationDay enumeration [Windows Update Agent], ausidEveryDay, ausidEveryFriday, ausidEveryMonday, ausidEverySaturday, ausidEverySunday, ausidEveryThursday, ausidEveryTuesday, ausidEveryWednesday, wua.automaticupdatesscheduledinstallationday, wuapi/AutomaticUpdatesScheduledInstallationDay, wuapi/ausidEveryDay, wuapi/ausidEveryFriday, wuapi/ausidEveryMonday, wuapi/ausidEverySaturday, wuapi/ausidEverySunday, wuapi/ausidEveryThursday, wuapi/ausidEveryTuesday, wuapi/ausidEveryWednesday
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
req.typenames: AutomaticUpdatesScheduledInstallationDay
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAutomaticUpdatesScheduledInstallationDay
 - wuapi/tagAutomaticUpdatesScheduledInstallationDay
 - AutomaticUpdatesScheduledInstallationDay
 - wuapi/AutomaticUpdatesScheduledInstallationDay
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
 - AutomaticUpdatesScheduledInstallationDay
---

# AutomaticUpdatesScheduledInstallationDay enumeration


## -description

Defines the days of the week when Automatic Updates installs or uninstalls updates.

## -enum-fields

### -field ausidEveryDay:0

Every day.

### -field ausidEverySunday:1

Every Sunday.

### -field ausidEveryMonday:2

Every Monday.

### -field ausidEveryTuesday:3

Every Tuesday.

### -field ausidEveryWednesday:4

Every Wednesday.

### -field ausidEveryThursday:5

Every Thursday.

### -field ausidEveryFriday:6

Every Friday.

### -field ausidEverySaturday:7

Every Saturday.

## -remarks

Updates are installed on the scheduled day. The updates depend on the settings of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> and <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">ScheduledInstallationTime</a> properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface.
