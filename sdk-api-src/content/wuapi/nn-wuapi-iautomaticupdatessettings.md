---
UID: NN:wuapi.IAutomaticUpdatesSettings
title: IAutomaticUpdatesSettings (wuapi.h)
description: Contains the settings that are available in Automatic Updates. (IAutomaticUpdatesSettings)
helpviewer_keywords: ["IAutomaticUpdatesSettings","IAutomaticUpdatesSettings interface [Windows Update Agent]","IAutomaticUpdatesSettings interface [Windows Update Agent]","described","wua.iautomaticupdatessettings","wuapi/IAutomaticUpdatesSettings"]
old-location: wua\iautomaticupdatessettings.htm
tech.root: wua
ms.assetid: c4672df5-9e47-45f5-9504-1ebb0bf3c6a6
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings, IAutomaticUpdatesSettings interface [Windows Update Agent], IAutomaticUpdatesSettings interface [Windows Update Agent],described, wua.iautomaticupdatessettings, wuapi/IAutomaticUpdatesSettings
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
 - IAutomaticUpdatesSettings
 - wuapi/IAutomaticUpdatesSettings
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
 - IAutomaticUpdatesSettings
---

# IAutomaticUpdatesSettings interface


## -description

 Contains the settings that are available in Automatic Updates.

## -inheritance

The <b>IAutomaticUpdatesSettings</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAutomaticUpdatesSettings</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Starting with Windows 8 and Windows Server 2012, <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday">ScheduledInstallationDay</a> and <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime">ScheduledInstallationTime</a> are not supported and will return unreliable values. If you try to modify these properties, the operation will appear to succeed but will have no effect.</div>
<div> </div>
<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">IAutomaticUpdatesSettings::Save</a> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">aunlScheduledInstallation</a>).</div>
<div> </div>
