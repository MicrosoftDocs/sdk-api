---
UID: NF:wuapi.IAutomaticUpdatesSettings.Save
title: IAutomaticUpdatesSettings::Save (wuapi.h)
description: Applies the current Automatic Updates settings.
helpviewer_keywords: ["IAutomaticUpdatesSettings interface [Windows Update Agent]","Save method","IAutomaticUpdatesSettings.Save","IAutomaticUpdatesSettings::Save","Save","Save method [Windows Update Agent]","Save method [Windows Update Agent]","IAutomaticUpdatesSettings interface","wua.iautomaticupdatessettings_save","wuapi/IAutomaticUpdatesSettings::Save"]
old-location: wua\iautomaticupdatessettings_save.htm
tech.root: wua
ms.assetid: fb54b900-345a-4b36-b16d-52790c0266f6
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],Save method, IAutomaticUpdatesSettings.Save, IAutomaticUpdatesSettings::Save, Save, Save method [Windows Update Agent], Save method [Windows Update Agent],IAutomaticUpdatesSettings interface, wua.iautomaticupdatessettings_save, wuapi/IAutomaticUpdatesSettings::Save
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
 - IAutomaticUpdatesSettings::Save
 - wuapi/IAutomaticUpdatesSettings::Save
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
 - IAutomaticUpdatesSettings.Save
---

# IAutomaticUpdatesSettings::Save


## -description

<p class="CCE_Message">[<b>AutomaticUpdatesSettings::Save</b> is no longer supported. Starting with 
    Windows 10 calls to <b>Save</b> always return 
    <b>S_OK</b>, but do nothing.]


Applies the current Automatic Updates settings.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

Saving settings with a <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> value other than Disabled  starts the Automatic Updates service.

<div class="alert"><b>Note</b>  On Windows RT, you can no longer use the <b>Save</b> method to configure Windows Update settings programmatically. The configuration operation fails if you use <b>Save</b> to set any value other than 4 (<a href="/windows/desktop/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel">aunlScheduledInstallation</a>).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
