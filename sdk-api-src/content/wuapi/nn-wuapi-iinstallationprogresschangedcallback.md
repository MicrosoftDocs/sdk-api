---
UID: NN:wuapi.IInstallationProgressChangedCallback
title: IInstallationProgressChangedCallback (wuapi.h)
description: Defines the Invoke method that handles the notification about the on-going progress of an asynchronous installation or uninstallation.
helpviewer_keywords: ["IInstallationProgressChangedCallback","IInstallationProgressChangedCallback interface [Windows Update Agent]","IInstallationProgressChangedCallback interface [Windows Update Agent]","described","wua.iinstallationprogresschangedcallback","wuapi/IInstallationProgressChangedCallback"]
old-location: wua\iinstallationprogresschangedcallback.htm
tech.root: wua
ms.assetid: a092dbba-57a4-4deb-be05-26cfa29e33aa
ms.date: 12/05/2018
ms.keywords: IInstallationProgressChangedCallback, IInstallationProgressChangedCallback interface [Windows Update Agent], IInstallationProgressChangedCallback interface [Windows Update Agent],described, wua.iinstallationprogresschangedcallback, wuapi/IInstallationProgressChangedCallback
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
 - IInstallationProgressChangedCallback
 - wuapi/IInstallationProgressChangedCallback
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
 - IInstallationProgressChangedCallback
---

# IInstallationProgressChangedCallback interface


## -description

Defines the <a href="/windows/desktop/api/wuapi/nf-wuapi-iinstallationprogresschangedcallback-invoke">Invoke</a> method that handles the notification about the on-going progress of an asynchronous installation or uninstallation. This interface is implemented by programmers who call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> method or the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> method.

## -inheritance

The <b>IInstallationProgressChangedCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInstallationProgressChangedCallback</b> also has these types of members:

