---
UID: NF:wuapi.IAutomaticUpdatesSettings.put_ScheduledInstallationDay
title: IAutomaticUpdatesSettings::put_ScheduledInstallationDay
author: windows-sdk-content
description: Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.
old-location: wua\iautomaticupdatessettings_scheduledinstallationday.htm
tech.root: wua_sdk
ms.assetid: 057498ad-d329-4fda-b3fe-95bdc27d62a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],ScheduledInstallationDay property, IAutomaticUpdatesSettings.ScheduledInstallationDay, IAutomaticUpdatesSettings.put_ScheduledInstallationDay, IAutomaticUpdatesSettings::ScheduledInstallationDay, IAutomaticUpdatesSettings::get_ScheduledInstallationDay, IAutomaticUpdatesSettings::put_ScheduledInstallationDay, ScheduledInstallationDay property [Windows Update Agent], ScheduledInstallationDay property [Windows Update Agent],IAutomaticUpdatesSettings interface, put_ScheduledInstallationDay, wua.iautomaticupdatessettings_scheduledinstallationday, wuapi/IAutomaticUpdatesSettings::ScheduledInstallationDay, wuapi/IAutomaticUpdatesSettings::get_ScheduledInstallationDay, wuapi/IAutomaticUpdatesSettings::put_ScheduledInstallationDay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

