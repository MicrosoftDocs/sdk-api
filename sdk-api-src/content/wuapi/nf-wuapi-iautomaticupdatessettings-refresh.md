---
UID: NF:wuapi.IAutomaticUpdatesSettings.Refresh
title: IAutomaticUpdatesSettings::Refresh (wuapi.h)
description: Retrieves the latest Automatic Updates settings.
helpviewer_keywords: ["IAutomaticUpdatesSettings interface [Windows Update Agent]","Refresh method","IAutomaticUpdatesSettings.Refresh","IAutomaticUpdatesSettings::Refresh","Refresh","Refresh method [Windows Update Agent]","Refresh method [Windows Update Agent]","IAutomaticUpdatesSettings interface","wua.iautomaticupdatessettings_refresh","wuapi/IAutomaticUpdatesSettings::Refresh"]
old-location: wua\iautomaticupdatessettings_refresh.htm
tech.root: wua
ms.assetid: 308426d9-d524-406a-931c-1fdb854aa4fb
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],Refresh method, IAutomaticUpdatesSettings.Refresh, IAutomaticUpdatesSettings::Refresh, Refresh, Refresh method [Windows Update Agent], Refresh method [Windows Update Agent],IAutomaticUpdatesSettings interface, wua.iautomaticupdatessettings_refresh, wuapi/IAutomaticUpdatesSettings::Refresh
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
 - IAutomaticUpdatesSettings::Refresh
 - wuapi/IAutomaticUpdatesSettings::Refresh
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
 - IAutomaticUpdatesSettings.Refresh
---

# IAutomaticUpdatesSettings::Refresh


## -description

Retrieves the latest Automatic Updates settings.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

Calling <b>Refresh</b>  resets any setting changes that have not been saved by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">Save</a> method.

<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">IAutomaticUpdatesSettings::Save</a> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">aunlScheduledInstallation</a>).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
