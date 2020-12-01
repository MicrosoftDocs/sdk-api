---
UID: NF:wuapi.IInstallationResult.GetUpdateResult
title: IInstallationResult::GetUpdateResult (wuapi.h)
description: Returns an IUpdateInstallationResult interface that contains the installation results for a specified update.
helpviewer_keywords: ["GetUpdateResult","GetUpdateResult method [Windows Update Agent]","GetUpdateResult method [Windows Update Agent]","IInstallationResult interface","IInstallationResult interface [Windows Update Agent]","GetUpdateResult method","IInstallationResult.GetUpdateResult","IInstallationResult::GetUpdateResult","wua.iinstallationresult_getupdateresult","wuapi/IInstallationResult::GetUpdateResult"]
old-location: wua\iinstallationresult_getupdateresult.htm
tech.root: wua
ms.assetid: 51d84e9e-9d92-43c9-af13-f833c3f3d631
ms.date: 12/05/2018
ms.keywords: GetUpdateResult, GetUpdateResult method [Windows Update Agent], GetUpdateResult method [Windows Update Agent],IInstallationResult interface, IInstallationResult interface [Windows Update Agent],GetUpdateResult method, IInstallationResult.GetUpdateResult, IInstallationResult::GetUpdateResult, wua.iinstallationresult_getupdateresult, wuapi/IInstallationResult::GetUpdateResult
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
 - IInstallationResult::GetUpdateResult
 - wuapi/IInstallationResult::GetUpdateResult
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
 - IInstallationResult.GetUpdateResult
---

# IInstallationResult::GetUpdateResult


## -description

Returns an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstallationresult">IUpdateInstallationResult</a> interface that contains the installation results  for a specified update.

## -parameters

### -param updateIndex [in]

The index of an update.

### -param retval [out]

An interface that contains results for a specified update.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationresult">IInstallationResult</a>