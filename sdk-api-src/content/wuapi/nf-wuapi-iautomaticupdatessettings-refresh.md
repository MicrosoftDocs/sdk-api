---
UID: NF:wuapi.IAutomaticUpdatesSettings.Refresh
title: IAutomaticUpdatesSettings::Refresh method
author: windows-driver-content
description: Retrieves the latest Automatic Updates settings.
old-location: wua\iautomaticupdatessettings_refresh.htm
old-project: Wua_Sdk
ms.assetid: 308426d9-d524-406a-931c-1fdb854aa4fb
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IAutomaticUpdatesSettings, IAutomaticUpdatesSettings interface [Windows Update Agent], Refresh method, IAutomaticUpdatesSettings::Refresh, Refresh method [Windows Update Agent], Refresh method [Windows Update Agent], IAutomaticUpdatesSettings interface, Refresh,IAutomaticUpdatesSettings.Refresh, wua.iautomaticupdatessettings_refresh, wuapi/IAutomaticUpdatesSettings::Refresh
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IAutomaticUpdatesSettings.Refresh
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAutomaticUpdatesSettings::Refresh method


## -description


Retrieves the latest Automatic Updates settings.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



Calling <b>Refresh</b>  resets any setting changes that have not been saved by using the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a> method.

<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <a href="https://msdn.microsoft.com/fb54b900-345a-4b36-b16d-52790c0266f6">IAutomaticUpdatesSettings::Save</a> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="automaticupdatesnotificationlevel.htm">aunlScheduledInstallation</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>
 

 

