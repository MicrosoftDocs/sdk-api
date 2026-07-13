---
UID: NF:wuapi.IAutomaticUpdates.DetectNow
title: IAutomaticUpdates::DetectNow (wuapi.h)
description: Begins the Automatic Updates detection task if Automatic Updates is enabled. If any updates are detected, the installation behavior is determined by the NotificationLevel property of the IAutomaticUpdatesSettings interface.
helpviewer_keywords: ["DetectNow","DetectNow method [Windows Update Agent]","DetectNow method [Windows Update Agent]","IAutomaticUpdates interface","IAutomaticUpdates interface [Windows Update Agent]","DetectNow method","IAutomaticUpdates.DetectNow","IAutomaticUpdates::DetectNow","wua.iautomaticupdates_detectnow","wuapi/IAutomaticUpdates::DetectNow"]
old-location: wua\iautomaticupdates_detectnow.htm
tech.root: wua
ms.assetid: ef40cd57-eab3-4ccf-a574-ab5237565e5b
ms.date: 12/05/2018
ms.keywords: DetectNow, DetectNow method [Windows Update Agent], DetectNow method [Windows Update Agent],IAutomaticUpdates interface, IAutomaticUpdates interface [Windows Update Agent],DetectNow method, IAutomaticUpdates.DetectNow, IAutomaticUpdates::DetectNow, wua.iautomaticupdates_detectnow, wuapi/IAutomaticUpdates::DetectNow
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
 - IAutomaticUpdates::DetectNow
 - wuapi/IAutomaticUpdates::DetectNow
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
 - IAutomaticUpdates.DetectNow
---

# IAutomaticUpdates::DetectNow


## -description

Begins the Automatic Updates detection task if Automatic Updates is enabled. If any updates are detected, the installation behavior is determined by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel">NotificationLevel</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a> interface.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the following conditions are true:

<ul>
<li>The <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is set to <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssManagedServer</a> or <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssDefault</a>.</li>
<li>The managed server on a computer is a Microsoft Software Update Services (SUS) version 1.0 server.</li>
</ul>
</td>
</tr>
</table>

## -remarks

This method returns <b>WU_E_AU_NOSERVICE</b> if Automatic Updates is disabled, initializing, uninitializing, or not configured.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">IAutomaticUpdates</a>
