---
UID: NF:cscobj.IOfflineFilesEvents2.SettingsChangesApplied
title: IOfflineFilesEvents2::SettingsChangesApplied
author: windows-sdk-content
description: Reports that the Offline Files service has applied the changes that were detected in Group Policy or preference values.
old-location: of\iofflinefilesevents2_settingschangesapplied.htm
tech.root: offlinefiles
ms.assetid: af59c8ac-ecd4-48e7-9ebb-8802e7d6ffef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesEvents2 interface [Offline Files],SettingsChangesApplied method, IOfflineFilesEvents2.SettingsChangesApplied, IOfflineFilesEvents2::SettingsChangesApplied, SettingsChangesApplied, SettingsChangesApplied method [Offline Files], SettingsChangesApplied method [Offline Files],IOfflineFilesEvents2 interface, cscobj/IOfflineFilesEvents2::SettingsChangesApplied, of.iofflinefilesevents2_settingschangesapplied
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents2.SettingsChangesApplied
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents2::SettingsChangesApplied


## -description


Reports that the Offline Files service has applied the changes that were detected in Group Policy or preference values.


## -parameters






## -returns



The return value is ignored.




## -remarks



After the Offline Files service reports that it has detected changes in Group Policy or preference settings, it waits for up to 5 seconds before it applies the changes to the system and calls this method. Therefore, up to 5 seconds can elapse between the last <a href="https://msdn.microsoft.com/en-us/library/Bb530529(v=VS.85).aspx">PolicyChangeDetected</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb530530(v=VS.85).aspx">PreferenceChangeDetected</a> event and the <b>SettingsChangesApplied</b> event.  An event listener should not make assumptions or perform any actions based on this time interval.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530521(v=VS.85).aspx">IOfflineFilesEvents2</a>
 

 

