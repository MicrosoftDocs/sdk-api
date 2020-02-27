---
UID: NE:wuapi.tagAutomaticUpdatesScheduledInstallationDay
title: AutomaticUpdatesScheduledInstallationDay (wuapi.h)
description: Defines the days of the week when Automatic Updates installs or uninstalls updates.
old-location: wua\automaticupdatesscheduledinstallationday.htm
tech.root: Wua_Sdk
ms.assetid: 8c7525bf-e15f-4c30-8e16-4b945d73f3cb
ms.date: 12/05/2018
ms.keywords: AutomaticUpdatesScheduledInstallationDay, AutomaticUpdatesScheduledInstallationDay enumeration [Windows Update Agent], ausidEveryDay, ausidEveryFriday, ausidEveryMonday, ausidEverySaturday, ausidEverySunday, ausidEveryThursday, ausidEveryTuesday, ausidEveryWednesday, wua.automaticupdatesscheduledinstallationday, wuapi/AutomaticUpdatesScheduledInstallationDay, wuapi/ausidEveryDay, wuapi/ausidEveryFriday, wuapi/ausidEveryMonday, wuapi/ausidEverySaturday, wuapi/ausidEverySunday, wuapi/ausidEveryThursday, wuapi/ausidEveryTuesday, wuapi/ausidEveryWednesday
f1_keywords:
- wuapi/AutomaticUpdatesScheduledInstallationDay
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wuapi.h
api_name:
- AutomaticUpdatesScheduledInstallationDay
targetos: Windows
req.typenames: AutomaticUpdatesScheduledInstallationDay
req.redist: 
ms.custom: 19H1
---

# AutomaticUpdatesScheduledInstallationDay enumeration


## -description


Defines the days of the week when Automatic Updates installs or uninstalls updates.


## -enum-fields




### -field ausidEveryDay

Every day.


### -field ausidEverySunday

Every Sunday.


### -field ausidEveryMonday

Every Monday.


### -field ausidEveryTuesday

Every Tuesday.


### -field ausidEveryWednesday

Every Wednesday.


### -field ausidEveryThursday

Every Thursday.


### -field ausidEveryFriday

Every Friday.


### -field ausidEverySaturday

Every Saturday.


## -remarks



Updates are installed on the scheduled day. The updates depend on the settings of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">ScheduledInstallationTime</a> properties of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface.



