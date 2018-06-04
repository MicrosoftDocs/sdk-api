---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

