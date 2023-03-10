---
UID: NF:wuapi.IUpdate.get_UninstallationBehavior
title: IUpdate::get_UninstallationBehavior (wuapi.h)
description: Gets an interface that contains the uninstallation options for the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","UninstallationBehavior property","IUpdate interface [Windows Update Services]","UninstallationBehavior property","IUpdate.UninstallationBehavior","IUpdate.get_UninstallationBehavior","IUpdate::UninstallationBehavior","IUpdate::get_UninstallationBehavior","UninstallationBehavior","UninstallationBehavior property [Windows Update Agent]","UninstallationBehavior property [Windows Update Agent]","IUpdate interface","UninstallationBehavior property [Windows Update Services]","UninstallationBehavior property [Windows Update Services]","IUpdate interface","get_UninstallationBehavior","wua.iupdate_uninstallationbehavior","wuapi/IUpdate::UninstallationBehavior","wuapi/IUpdate::get_UninstallationBehavior"]
old-location: wua\iupdate_uninstallationbehavior.htm
tech.root: wua
ms.assetid: 12f35005-5dea-42c9-8c3b-eeb28bdd93b3
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],UninstallationBehavior property, IUpdate interface [Windows Update Services],UninstallationBehavior property, IUpdate.UninstallationBehavior, IUpdate.get_UninstallationBehavior, IUpdate::UninstallationBehavior, IUpdate::get_UninstallationBehavior, UninstallationBehavior, UninstallationBehavior property [Windows Update Agent], UninstallationBehavior property [Windows Update Agent],IUpdate interface, UninstallationBehavior property [Windows Update Services], UninstallationBehavior property [Windows Update Services],IUpdate interface, get_UninstallationBehavior, wua.iupdate_uninstallationbehavior, wuapi/IUpdate::UninstallationBehavior, wuapi/IUpdate::get_UninstallationBehavior
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
 - IUpdate::get_UninstallationBehavior
 - wuapi/IUpdate::get_UninstallationBehavior
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
 - IUpdate.UninstallationBehavior
 - IUpdate.get_UninstallationBehavior
---

# IUpdate::get_UninstallationBehavior


## -description

Gets an interface that contains the uninstallation options for the update.

This property is read-only.

## -parameters

## -returns

Returns S_OK if successful. Otherwise, returns a COM or Windows error code.

## -remarks

This API can return a null pointer as the output, even when the return value is S_OK.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
