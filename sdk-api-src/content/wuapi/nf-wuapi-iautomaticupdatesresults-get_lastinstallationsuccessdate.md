---
UID: NF:wuapi.IAutomaticUpdatesResults.get_LastInstallationSuccessDate
title: IAutomaticUpdatesResults::get_LastInstallationSuccessDate (wuapi.h)
description: Gets the last time and Coordinated Universal Time (UTC) date when Automatic Updates successfully installed any updates, even if some failures occurred.
helpviewer_keywords: ["IAutomaticUpdatesResults interface [Windows Update Agent]","LastInstallationSuccessDate property","IAutomaticUpdatesResults.LastInstallationSuccessDate","IAutomaticUpdatesResults.get_LastInstallationSuccessDate","IAutomaticUpdatesResults::LastInstallationSuccessDate","IAutomaticUpdatesResults::get_LastInstallationSuccessDate","LastInstallationSuccessDate property [Windows Update Agent]","LastInstallationSuccessDate property [Windows Update Agent]","IAutomaticUpdatesResults interface","get_LastInstallationSuccessDate","wua.iautomaticupdatesresults_lastinstallationsuccessdate","wuapi/IAutomaticUpdatesResults::LastInstallationSuccessDate","wuapi/IAutomaticUpdatesResults::get_LastInstallationSuccessDate"]
old-location: wua\iautomaticupdatesresults_lastinstallationsuccessdate.htm
tech.root: wua
ms.assetid: 31cd54fa-ad4a-4a60-a87e-7c915cf596d7
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesResults interface [Windows Update Agent],LastInstallationSuccessDate property, IAutomaticUpdatesResults.LastInstallationSuccessDate, IAutomaticUpdatesResults.get_LastInstallationSuccessDate, IAutomaticUpdatesResults::LastInstallationSuccessDate, IAutomaticUpdatesResults::get_LastInstallationSuccessDate, LastInstallationSuccessDate property [Windows Update Agent], LastInstallationSuccessDate property [Windows Update Agent],IAutomaticUpdatesResults interface, get_LastInstallationSuccessDate, wua.iautomaticupdatesresults_lastinstallationsuccessdate, wuapi/IAutomaticUpdatesResults::LastInstallationSuccessDate, wuapi/IAutomaticUpdatesResults::get_LastInstallationSuccessDate
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
 - IAutomaticUpdatesResults::get_LastInstallationSuccessDate
 - wuapi/IAutomaticUpdatesResults::get_LastInstallationSuccessDate
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
 - IAutomaticUpdatesResults.LastInstallationSuccessDate
 - IAutomaticUpdatesResults.get_LastInstallationSuccessDate
---

# IAutomaticUpdatesResults::get_LastInstallationSuccessDate


## -description

Gets the last time and Coordinated Universal Time (UTC) date when Automatic Updates successfully installed any updates, even if some failures occurred.

This property is read-only.

## -parameters

## -remarks

Calls to <b>LastInstallationSuccessDate</b> by public users do not update this property. Only the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">AutomaticUpdates</a> object will update this property.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatesresults">IAutomaticUpdatesResults</a>