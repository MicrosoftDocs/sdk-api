---
UID: NF:wuapi.IAutomaticUpdates.DetectNow
title: IAutomaticUpdates::DetectNow
author: windows-sdk-content
description: Begins the Automatic Updates detection task if Automatic Updates is enabled. If any updates are detected, the installation behavior is determined by the NotificationLevel property of the IAutomaticUpdatesSettings interface.
old-location: wua\iautomaticupdates_detectnow.htm
tech.root: wua_sdk
ms.assetid: ef40cd57-eab3-4ccf-a574-ab5237565e5b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DetectNow, DetectNow method [Windows Update Agent], DetectNow method [Windows Update Agent],IAutomaticUpdates interface, IAutomaticUpdates interface [Windows Update Agent],DetectNow method, IAutomaticUpdates.DetectNow, IAutomaticUpdates::DetectNow, wua.iautomaticupdates_detectnow, wuapi/IAutomaticUpdates::DetectNow
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
 - IAutomaticUpdates.DetectNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutomaticUpdates::DetectNow


## -description


Begins the Automatic Updates detection task if Automatic Updates is enabled. If any updates are detected, the installation behavior is determined by the <a href="https://msdn.microsoft.com/da4fdb8a-8df8-468f-afde-292bbcf6696b">NotificationLevel</a> property of the <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a> interface.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the following conditions are true:

<ul>
<li>The <a href="https://msdn.microsoft.com/b514545a-d983-491b-9a28-540bd5c4c128">ServerSelection</a> property of the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface is set to <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ssManagedServer</a> or <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ssDefault</a>.</li>
<li>The managed server on a computer is a Microsoft Software Update Services (SUS) version 1.0 server.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_AU_NOSERVICE</b> if Automatic Updates is disabled, initializing, uninitializing, or not configured.




## -see-also




<a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">IAutomaticUpdates</a>
 

 

