---
UID: NF:wuapi.IAutomaticUpdatesSettings.get_ReadOnly
title: IAutomaticUpdatesSettings::get_ReadOnly (wuapi.h)
description: Gets a Boolean value that indicates whether the Automatic Update settings are read-only.
helpviewer_keywords: ["IAutomaticUpdatesSettings interface [Windows Update Agent]","ReadOnly property","IAutomaticUpdatesSettings.ReadOnly","IAutomaticUpdatesSettings.get_ReadOnly","IAutomaticUpdatesSettings::ReadOnly","IAutomaticUpdatesSettings::get_ReadOnly","ReadOnly property [Windows Update Agent]","ReadOnly property [Windows Update Agent]","IAutomaticUpdatesSettings interface","get_ReadOnly","wua.iautomaticupdatessettings_readonly","wuapi/IAutomaticUpdatesSettings::ReadOnly","wuapi/IAutomaticUpdatesSettings::get_ReadOnly"]
old-location: wua\iautomaticupdatessettings_readonly.htm
tech.root: wua
ms.assetid: e7a066b9-9581-4573-82e2-a6f2ca7440ac
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],ReadOnly property, IAutomaticUpdatesSettings.ReadOnly, IAutomaticUpdatesSettings.get_ReadOnly, IAutomaticUpdatesSettings::ReadOnly, IAutomaticUpdatesSettings::get_ReadOnly, ReadOnly property [Windows Update Agent], ReadOnly property [Windows Update Agent],IAutomaticUpdatesSettings interface, get_ReadOnly, wua.iautomaticupdatessettings_readonly, wuapi/IAutomaticUpdatesSettings::ReadOnly, wuapi/IAutomaticUpdatesSettings::get_ReadOnly
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
 - IAutomaticUpdatesSettings::get_ReadOnly
 - wuapi/IAutomaticUpdatesSettings::get_ReadOnly
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
 - IAutomaticUpdatesSettings.ReadOnly
 - IAutomaticUpdatesSettings.get_ReadOnly
---

# IAutomaticUpdatesSettings::get_ReadOnly


## -description

<p class="CCE_Message">[<b>IAutomaticUpdatesSettings::ReadOnly</b> is no longer supported. Starting with 
    Windows 10 calls to <b>ReadOnly</b> always return <b>VARIANT_FALSE</b>. However, <b>IAutomaticUpdatesSettings::Save</b> is a no-op, so no changes can be made.]


Gets a Boolean value that indicates whether the Automatic Update settings are read-only.



This property is read-only.

## -parameters

## -remarks

<b>ReadOnly</b> is <b>VARIANT_TRUE</b> if either of the following conditions is true:

<ul>
<li>The caller has insufficient security permissions to modify the Automatic Updates settings.</li>
<li>The current settings are enforced by Group Policy.
</li>
</ul>
 
The caller can modify the settings in the  <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface only if <b>ReadOnly</b> is <b>VARIANT_FALSE</b>.
The value of <b>ReadOnly</b> may change after calling <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-refresh">Refresh</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-refresh">IAutomaticUpdatesSettings.Refresh</a>