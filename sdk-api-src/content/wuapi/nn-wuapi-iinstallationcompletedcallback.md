---
UID: NN:wuapi.IInstallationCompletedCallback
title: IInstallationCompletedCallback
author: windows-driver-content
description: Handles the notification that indicates that an asynchronous installation or uninstallation is complete.
old-location: wua\iinstallationcompletedcallback.htm
old-project: Wua_Sdk
ms.assetid: 930d33e1-e407-4306-acc6-1d64c385a41d
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IInstallationCompletedCallback, IInstallationCompletedCallback interface [Windows Update Agent], IInstallationCompletedCallback interface [Windows Update Agent],described, wua.iinstallationcompletedcallback, wuapi/IInstallationCompletedCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IInstallationCompletedCallback
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IInstallationCompletedCallback interface


## -description


Handles the notification that indicates that an asynchronous installation or uninstallation is complete.   This interface is implemented by programmers who call the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationCompletedCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInstallationCompletedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInstallationCompletedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7c413b2-b485-41a5-b2c9-5c3e9c10427c">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of the completion of an asynchronous installation or uninstallation initiated by a call to <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a>.

</td>
</tr>
</table> 

