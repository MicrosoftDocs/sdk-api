---
UID: NN:wuapi.IUpdateInstaller3
title: IUpdateInstaller3
author: windows-sdk-content
description: Installs or uninstalls updates on a computer.
old-location: wua\iupdateinstaller3.htm
old-project: Wua_Sdk
ms.assetid: 5A237B5C-A07B-470F-B2F6-ABC936DCE1A5
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IUpdateInstaller3, IUpdateInstaller3 interface [Windows Update Agent], IUpdateInstaller3 interface [Windows Update Agent],described, wua.iupdateinstaller3, wuapi/IUpdateInstaller3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - IUpdateInstaller3
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller3 interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Installs or uninstalls updates on a computer. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateInstaller3</b> interface inherits from <a href="https://msdn.microsoft.com/89edc91d-59a1-4e23-9adb-fc3027e2e898">IUpdateInstaller2</a>. <b>IUpdateInstaller3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateInstaller3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="wua.iupdateinstaller3_get_attemptcloseappsifnecessary">get_AttemptCloseAppsIfNecessary</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="wua.iupdateinstaller3_put_attemptcloseappsifnecessary">put_AttemptCloseAppsIfNecessary</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/89edc91d-59a1-4e23-9adb-fc3027e2e898">IUpdateInstaller2</a>
 

 

