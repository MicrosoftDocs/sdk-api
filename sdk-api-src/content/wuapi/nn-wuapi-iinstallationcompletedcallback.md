---
UID: NN:wuapi.IInstallationCompletedCallback
title: IInstallationCompletedCallback (wuapi.h)
description: Handles the notification that indicates that an asynchronous installation or uninstallation is complete.
helpviewer_keywords: ["IInstallationCompletedCallback","IInstallationCompletedCallback interface [Windows Update Agent]","IInstallationCompletedCallback interface [Windows Update Agent]","described","wua.iinstallationcompletedcallback","wuapi/IInstallationCompletedCallback"]
old-location: wua\iinstallationcompletedcallback.htm
tech.root: wua
ms.assetid: 930d33e1-e407-4306-acc6-1d64c385a41d
ms.date: 12/05/2018
ms.keywords: IInstallationCompletedCallback, IInstallationCompletedCallback interface [Windows Update Agent], IInstallationCompletedCallback interface [Windows Update Agent],described, wua.iinstallationcompletedcallback, wuapi/IInstallationCompletedCallback
f1_keywords:
- wuapi/IInstallationCompletedCallback
dev_langs:
- c++
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
- IInstallationCompletedCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationCompletedCallback interface


## -description


Handles the notification that indicates that an asynchronous installation or uninstallation is complete.   This interface is implemented by programmers who call the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationCompletedCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInstallationCompletedCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationcompletedcallback-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of the completion of an asynchronous installation or uninstallation initiated by a call to <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a>.

</td>
</tr>
</table> 

