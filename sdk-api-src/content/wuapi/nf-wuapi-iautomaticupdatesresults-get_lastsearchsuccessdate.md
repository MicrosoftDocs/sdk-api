---
UID: NF:wuapi.IAutomaticUpdatesResults.get_LastSearchSuccessDate
title: IAutomaticUpdatesResults::get_LastSearchSuccessDate
author: windows-sdk-content
description: Gets the last time and Coordinated Universal Time (UTC) date when AutomaticUpdates successfully searched for updates.
old-location: wua\iautomaticupdatesresults_lastsearchsuccessdate.htm
old-project: wua_sdk
ms.assetid: 3c053888-be91-45e9-a5da-182f18e07710
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IAutomaticUpdatesResults interface [Windows Update Agent],LastSearchSuccessDate property, IAutomaticUpdatesResults.LastSearchSuccessDate, IAutomaticUpdatesResults.get_LastSearchSuccessDate, IAutomaticUpdatesResults::LastSearchSuccessDate, IAutomaticUpdatesResults::get_LastSearchSuccessDate, LastSearchSuccessDate property [Windows Update Agent], LastSearchSuccessDate property [Windows Update Agent],IAutomaticUpdatesResults interface, get_LastSearchSuccessDate, wua.iautomaticupdatesresults_lastsearchsuccessdate, wuapi/IAutomaticUpdatesResults::LastSearchSuccessDate, wuapi/IAutomaticUpdatesResults::get_LastSearchSuccessDate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesResults.LastSearchSuccessDate
 - IAutomaticUpdatesResults.get_LastSearchSuccessDate
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAutomaticUpdatesResults::get_LastSearchSuccessDate


## -description


Gets the last time and Coordinated Universal Time (UTC) date when AutomaticUpdates successfully searched for updates.

This property is read-only.


## -parameters


## -remarks



Calls to <b>LastSearchSuccessDate</b> by public users do not update this property. Only the <a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">AutomaticUpdates</a> object will update this property.




## -see-also




<a href="https://msdn.microsoft.com/fe9a5ea3-9d59-450b-8c5e-3444ec13dc97">IAutomaticUpdatesResults</a>
 

 

