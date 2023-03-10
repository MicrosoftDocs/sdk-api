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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInstallationCompletedCallback
 - wuapi/IInstallationCompletedCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationCompletedCallback
---

# IInstallationCompletedCallback interface


## -description

Handles the notification that indicates that an asynchronous installation or uninstallation is complete.   This interface is implemented by programmers who call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> methods.

## -inheritance

The <b>IInstallationCompletedCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInstallationCompletedCallback</b> also has these types of members:

