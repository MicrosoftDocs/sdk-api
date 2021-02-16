---
UID: NF:wuapi.IAutomaticUpdatesResults.get_LastSearchSuccessDate
title: IAutomaticUpdatesResults::get_LastSearchSuccessDate (wuapi.h)
description: Gets the last time and Coordinated Universal Time (UTC) date when AutomaticUpdates successfully searched for updates.
helpviewer_keywords: ["IAutomaticUpdatesResults interface [Windows Update Agent]","LastSearchSuccessDate property","IAutomaticUpdatesResults.LastSearchSuccessDate","IAutomaticUpdatesResults.get_LastSearchSuccessDate","IAutomaticUpdatesResults::LastSearchSuccessDate","IAutomaticUpdatesResults::get_LastSearchSuccessDate","LastSearchSuccessDate property [Windows Update Agent]","LastSearchSuccessDate property [Windows Update Agent]","IAutomaticUpdatesResults interface","get_LastSearchSuccessDate","wua.iautomaticupdatesresults_lastsearchsuccessdate","wuapi/IAutomaticUpdatesResults::LastSearchSuccessDate","wuapi/IAutomaticUpdatesResults::get_LastSearchSuccessDate"]
old-location: wua\iautomaticupdatesresults_lastsearchsuccessdate.htm
tech.root: wua
ms.assetid: 3c053888-be91-45e9-a5da-182f18e07710
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesResults interface [Windows Update Agent],LastSearchSuccessDate property, IAutomaticUpdatesResults.LastSearchSuccessDate, IAutomaticUpdatesResults.get_LastSearchSuccessDate, IAutomaticUpdatesResults::LastSearchSuccessDate, IAutomaticUpdatesResults::get_LastSearchSuccessDate, LastSearchSuccessDate property [Windows Update Agent], LastSearchSuccessDate property [Windows Update Agent],IAutomaticUpdatesResults interface, get_LastSearchSuccessDate, wua.iautomaticupdatesresults_lastsearchsuccessdate, wuapi/IAutomaticUpdatesResults::LastSearchSuccessDate, wuapi/IAutomaticUpdatesResults::get_LastSearchSuccessDate
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
 - IAutomaticUpdatesResults::get_LastSearchSuccessDate
 - wuapi/IAutomaticUpdatesResults::get_LastSearchSuccessDate
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
 - IAutomaticUpdatesResults.LastSearchSuccessDate
 - IAutomaticUpdatesResults.get_LastSearchSuccessDate
---

# IAutomaticUpdatesResults::get_LastSearchSuccessDate


## -description

Gets the last time and Coordinated Universal Time (UTC) date when AutomaticUpdates successfully searched for updates.

This property is read-only.

## -parameters

## -remarks

Calls to <b>LastSearchSuccessDate</b> by public users do not update this property. Only the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">AutomaticUpdates</a> object will update this property.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatesresults">IAutomaticUpdatesResults</a>