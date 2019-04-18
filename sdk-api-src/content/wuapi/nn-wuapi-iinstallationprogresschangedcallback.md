---
UID: NN:wuapi.IInstallationProgressChangedCallback
title: IInstallationProgressChangedCallback (wuapi.h)
author: windows-sdk-content
description: Defines the Invoke method that handles the notification about the on-going progress of an asynchronous installation or uninstallation.
old-location: wua\iinstallationprogresschangedcallback.htm
tech.root: Wua_Sdk
ms.assetid: a092dbba-57a4-4deb-be05-26cfa29e33aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInstallationProgressChangedCallback, IInstallationProgressChangedCallback interface [Windows Update Agent], IInstallationProgressChangedCallback interface [Windows Update Agent],described, wua.iinstallationprogresschangedcallback, wuapi/IInstallationProgressChangedCallback
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
 - IInstallationProgressChangedCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationProgressChangedCallback interface


## -description


Defines the <a href="https://msdn.microsoft.com/1ef4ab68-8bf3-4141-aba2-826bb606eab5">Invoke</a> method that handles the notification about the on-going progress of an asynchronous installation or uninstallation. This interface is implemented by programmers who call the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> method or the <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationProgressChangedCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInstallationProgressChangedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInstallationProgressChangedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef4ab68-8bf3-4141-aba2-826bb606eab5">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of the change of progress of an asynchronous installation or uninstallation that was initiated by a call to the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method.

</td>
</tr>
</table> 

