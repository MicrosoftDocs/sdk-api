---
UID: NE:wuapi.tagAutomaticUpdatesNotificationLevel
title: tagAutomaticUpdatesNotificationLevel
author: windows-sdk-content
description: Defines the possible ways in which elevated users are notified about Automatic Updates events.
old-location: wua\automaticupdatesnotificationlevel.htm
tech.root: wua_sdk
ms.assetid: a326400b-d6df-4947-8ab8-126d357834c3
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: AutomaticUpdatesNotificationLevel, AutomaticUpdatesNotificationLevel enumeration [Windows Update Agent], aunlDisabled, aunlNotConfigured, aunlNotifyBeforeDownload, aunlNotifyBeforeInstallation, aunlScheduledInstallation, tagAutomaticUpdatesNotificationLevel, wua.automaticupdatesnotificationlevel, wuapi/AutomaticUpdatesNotificationLevel, wuapi/aunlDisabled, wuapi/aunlNotConfigured, wuapi/aunlNotifyBeforeDownload, wuapi/aunlNotifyBeforeInstallation, wuapi/aunlScheduledInstallation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - AutomaticUpdatesNotificationLevel
product: Windows
targetos: Windows
req.typenames: AutomaticUpdatesNotificationLevel
req.redist: 
---

# tagAutomaticUpdatesNotificationLevel enumeration


## -description


Defines the possible ways in which elevated users are notified about   Automatic Updates events.


## -enum-fields




### -field aunlNotConfigured

Automatic Updates is not configured by the user or by a Group Policy administrator. Users are periodically prompted to configure Automatic Updates.


### -field aunlDisabled

Automatic Updates is disabled. Users are not  notified of important updates for the computer.


### -field aunlNotifyBeforeDownload

Automatic Updates  prompts users to approve updates before it downloads or installs the updates.


### -field aunlNotifyBeforeInstallation

Automatic Updates  automatically downloads updates, but  prompts users to approve the updates before installation.


### -field aunlScheduledInstallation

Automatic Updates  automatically installs updates according to the schedule that is specified by the user or by the <a href="https://msdn.microsoft.com/057498ad-d329-4fda-b3fe-95bdc27d62a4">IAutomaticUpdatesSettings.ScheduledInstallationDay</a> and <a href="https://msdn.microsoft.com/1b1adefc-785e-46ad-8984-d2beb1c2202c">IAutomaticUPdatesSettings.ScheduledInstallationTime</a> properties. This setting is the recommended setting.

