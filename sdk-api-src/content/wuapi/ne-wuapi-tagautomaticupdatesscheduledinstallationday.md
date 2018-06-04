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

# tagAutomaticUpdatesScheduledInstallationDay enumeration


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



Updates are installed on the scheduled day. The updates depend on the settings of the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">NotificationLevel</a> and <a href="https://msdn.microsoft.com/1b1adefc-785e-46ad-8984-d2beb1c2202c">ScheduledInstallationTime</a> properties of the <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a> interface.



