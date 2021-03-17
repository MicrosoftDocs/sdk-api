---
UID: NF:wuapi.IUpdateInstaller.get_IsBusy
title: IUpdateInstaller::get_IsBusy (wuapi.h)
description: Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.
helpviewer_keywords: ["IUpdateInstaller interface [Windows Update Agent]","IsBusy property","IUpdateInstaller.IsBusy","IUpdateInstaller.get_IsBusy","IUpdateInstaller::IsBusy","IUpdateInstaller::get_IsBusy","IsBusy property [Windows Update Agent]","IsBusy property [Windows Update Agent]","IUpdateInstaller interface","get_IsBusy","wua.iupdateinstaller_isbusy","wuapi/IUpdateInstaller::IsBusy","wuapi/IUpdateInstaller::get_IsBusy"]
old-location: wua\iupdateinstaller_isbusy.htm
tech.root: wua
ms.assetid: 20875312-f54a-45fc-a0f4-ed17b812dd9e
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller interface [Windows Update Agent],IsBusy property, IUpdateInstaller.IsBusy, IUpdateInstaller.get_IsBusy, IUpdateInstaller::IsBusy, IUpdateInstaller::get_IsBusy, IsBusy property [Windows Update Agent], IsBusy property [Windows Update Agent],IUpdateInstaller interface, get_IsBusy, wua.iupdateinstaller_isbusy, wuapi/IUpdateInstaller::IsBusy, wuapi/IUpdateInstaller::get_IsBusy
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
 - IUpdateInstaller::get_IsBusy
 - wuapi/IUpdateInstaller::get_IsBusy
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
 - IUpdateInstaller.IsBusy
 - IUpdateInstaller.get_IsBusy
---

# IUpdateInstaller::get_IsBusy


## -description

Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.

This property is read-only.

## -parameters

## -remarks

A new installation or uninstallation is processed only when no other installation or uninstallation is in progress. While an installation or uninstallation is in progress, a new installation or uninstallation immediately fails with the <b>WU_E_OPERATIONINPROGRESS</b> error. The <b>IsBusy</b> property does not secure an opportunity for the caller to begin a new installation or uninstallation. If the <b>IsBusy</b> property or a recent installation or uninstallation failure indicates that another installation or uninstallation is already in progress, the caller should attempt the installation or uninstallation later.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>