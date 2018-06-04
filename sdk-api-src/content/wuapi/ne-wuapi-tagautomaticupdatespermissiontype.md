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

# tagAutomaticUpdatesPermissionType enumeration


## -description


Defines the possible ways to set the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">NotificationLevel</a> property of the <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a> interface or the <a href="https://msdn.microsoft.com/502b0490-8834-496a-8691-d9325ad86799">IncludeRecommendedUpdates</a> property of the <a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a> interface.


## -enum-fields




### -field auptSetNotificationLevel

The ability to set the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">IAutomaticUpdatesSettings::NotificationLevel</a> property.


### -field auptDisableAutomaticUpdates

The ability to set the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">IAutomaticUpdatesSettings::NotificationLevel</a> property to <a href="automaticupdatesnotificationlevel.htm">aunlDisabled</a>.


### -field auptSetIncludeRecommendedUpdates

The ability to set the <a href="https://msdn.microsoft.com/502b0490-8834-496a-8691-d9325ad86799">IAutomaticUpdatesSettings2::IncludedRecommendedUpdates</a> property.


### -field auptSetFeaturedUpdatesEnabled

The ability to set the <a href="https://msdn.microsoft.com/43f17feb-1a3b-4399-a26f-1a2d99442169">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> property.


### -field auptSetNonAdministratorsElevated

The ability to set the <a href="https://msdn.microsoft.com/6294d982-e6ed-472d-b94b-c140b423ea88">IAutomaticUpdatesSettings3::NonAdministratorsElevated</a> property.


## -remarks



Featured update notifications are only supported on Windows Vista and above. On Windows XP systems running versions of the Windows Update Agent (WUA) that support <a href="https://msdn.microsoft.com/2cc4d15f-eb8c-4db1-a81b-6eb3ee128121">IAutomaticUpdatesSettings3</a>, the <a href="https://msdn.microsoft.com/43f17feb-1a3b-4399-a26f-1a2d99442169">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.

Featured update notifications are only supported when Automatic Updates is turned on. If Automatic Updates is set to “Never check for updates (not recommended),” then the <a href="https://msdn.microsoft.com/43f17feb-1a3b-4399-a26f-1a2d99442169">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.

Featured update notifications are only supported on certain update services. Currently, the only supported update service is Microsoft Update. If Automatic Updates is currently configured to receive updates from another service (from Windows Update, or from a WSUS server), then  the <a href="https://msdn.microsoft.com/43f17feb-1a3b-4399-a26f-1a2d99442169">IAutomaticUpdatesSettings3::FeaturedUpdatesEnabled</a> value will always be VARIANT_FALSE, and attempting to alter its value will result in an error.



