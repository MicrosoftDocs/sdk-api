---
UID: NF:wuapi.IUpdate.get_InstallationBehavior
title: IUpdate::get_InstallationBehavior (wuapi.h)
description: Gets an interface that contains the installation options of the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","InstallationBehavior property","IUpdate.InstallationBehavior","IUpdate.get_InstallationBehavior","IUpdate::InstallationBehavior","IUpdate::get_InstallationBehavior","InstallationBehavior property [Windows Update Agent]","InstallationBehavior property [Windows Update Agent]","IUpdate interface","get_InstallationBehavior","wua.iupdate_installationbehavior","wuapi/IUpdate::InstallationBehavior","wuapi/IUpdate::get_InstallationBehavior"]
old-location: wua\iupdate_installationbehavior.htm
tech.root: wua
ms.assetid: f02e5ebc-a8ea-496b-a79e-52644b98e75d
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],InstallationBehavior property, IUpdate.InstallationBehavior, IUpdate.get_InstallationBehavior, IUpdate::InstallationBehavior, IUpdate::get_InstallationBehavior, InstallationBehavior property [Windows Update Agent], InstallationBehavior property [Windows Update Agent],IUpdate interface, get_InstallationBehavior, wua.iupdate_installationbehavior, wuapi/IUpdate::InstallationBehavior, wuapi/IUpdate::get_InstallationBehavior
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
 - IUpdate::get_InstallationBehavior
 - wuapi/IUpdate::get_InstallationBehavior
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
 - IUpdate.InstallationBehavior
 - IUpdate.get_InstallationBehavior
---

# IUpdate::get_InstallationBehavior


## -description

Gets an interface that contains the installation options of the update.

This property is read-only.

## -parameters

## -returns

Returns S_OK if successful. Otherwise, returns a COM or Windows error code.

## -remarks

If the current update represents a bundle, the <b>InstallationBehavior</b> property of the bundle will be determined by the <b>InstallationBehavior</b> property of the child updates of the bundle. This API can return a null pointer as the output, even when the return value is S_OK.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
