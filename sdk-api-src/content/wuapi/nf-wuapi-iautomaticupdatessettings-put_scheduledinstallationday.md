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

# IAutomaticUpdatesSettings::put_ScheduledInstallationDay


## -description


<p class="CCE_Message">[<b>IAutomaticUpdatesSettings::ScheduledInstallationDay</b> is no longer supported as of Windows 10.]


Gets and sets the days of the week on which Automatic Updates  installs or uninstalls updates.



This property is read/write.


## -parameters


## -remarks



The value of this property is ignored if the value of the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">NotificationLevel</a> property is not <b>aunlScheduledInstallation</b>.

<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <b>ScheduledInstallationDay</b> is not supported and will return unreliable values. If you try to modify <b>ScheduledInstallationDay</b>, the operation will appear to succeed but will have no effect.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>
 

 

