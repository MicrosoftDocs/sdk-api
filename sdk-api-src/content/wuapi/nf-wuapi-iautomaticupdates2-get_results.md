---
UID: NF:wuapi.IAutomaticUpdates2.get_Results
title: IAutomaticUpdates2::get_Results (wuapi.h)
description: Returns a pointer to an IAutomaticUpdatesResults interface.
helpviewer_keywords: ["IAutomaticUpdates2 interface [Windows Update Agent]","get_Results method","IAutomaticUpdates2.get_Results","IAutomaticUpdates2::get_Results","get_Results","get_Results method [Windows Update Agent]","get_Results method [Windows Update Agent]","IAutomaticUpdates2 interface","wua.iautomaticupdates2_results","wuapi/IAutomaticUpdates2::get_Results"]
old-location: wua\iautomaticupdates2_results.htm
tech.root: wua
ms.assetid: b83f6833-5318-42ca-a1d6-30b6590873bb
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdates2 interface [Windows Update Agent],get_Results method, IAutomaticUpdates2.get_Results, IAutomaticUpdates2::get_Results, get_Results, get_Results method [Windows Update Agent], get_Results method [Windows Update Agent],IAutomaticUpdates2 interface, wua.iautomaticupdates2_results, wuapi/IAutomaticUpdates2::get_Results
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
 - IAutomaticUpdates2::get_Results
 - wuapi/IAutomaticUpdates2::get_Results
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
 - IAutomaticUpdates2.get_Results
---

# IAutomaticUpdates2::get_Results


## -description

Returns a pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatesresults">IAutomaticUpdatesResults</a> interface.

## -parameters

### -param retval [out]

A pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatesresults">IAutomaticUpdatesResults</a> interface.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates2">IAutomaticUpdates2</a>