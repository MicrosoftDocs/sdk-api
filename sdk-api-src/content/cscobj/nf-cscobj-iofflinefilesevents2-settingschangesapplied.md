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

# IOfflineFilesEvents2::SettingsChangesApplied


## -description


Reports that the Offline Files service has applied the changes that were detected in Group Policy or preference values.


## -parameters






## -returns



The return value is ignored.




## -remarks



After the Offline Files service reports that it has detected changes in Group Policy or preference settings, it waits for up to 5 seconds before it applies the changes to the system and calls this method. Therefore, up to 5 seconds can elapse between the last <a href="https://msdn.microsoft.com/1009c67a-09f4-40ea-8aa9-fb42f1ab54ff">PolicyChangeDetected</a> or <a href="https://msdn.microsoft.com/c947d9e5-2712-4dbd-8806-79a8bf0f4cc9">PreferenceChangeDetected</a> event and the <b>SettingsChangesApplied</b> event.  An event listener should not make assumptions or perform any actions based on this time interval.




## -see-also




<a href="https://msdn.microsoft.com/746f7220-8c87-4218-bd97-ec9b862e549c">IOfflineFilesEvents2</a>
 

 

