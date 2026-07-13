---
UID: NF:wuapi.IAutomaticUpdates.Pause
title: IAutomaticUpdates::Pause (wuapi.h)
description: Pauses automatic updates.
helpviewer_keywords: ["IAutomaticUpdates interface [Windows Update Agent]","Pause method","IAutomaticUpdates.Pause","IAutomaticUpdates::Pause","Pause","Pause method [Windows Update Agent]","Pause method [Windows Update Agent]","IAutomaticUpdates interface","wua.iautomaticupdates_pause","wuapi/IAutomaticUpdates::Pause"]
old-location: wua\iautomaticupdates_pause.htm
tech.root: wua
ms.assetid: 42985fdf-b3b3-43f0-addb-478298bd8ebd
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdates interface [Windows Update Agent],Pause method, IAutomaticUpdates.Pause, IAutomaticUpdates::Pause, Pause, Pause method [Windows Update Agent], Pause method [Windows Update Agent],IAutomaticUpdates interface, wua.iautomaticupdates_pause, wuapi/IAutomaticUpdates::Pause
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAutomaticUpdates::Pause
 - wuapi/IAutomaticUpdates::Pause
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
 - IAutomaticUpdates.Pause
---

# IAutomaticUpdates::Pause


## -description

<p class="CCE_Message">[<b>IAutomaticUpdates::Pause</b> is no longer supported. Starting with 
    Windows 10 calls to <b>Pause</b> always return 
    <b>S_OK</b>, but do nothing.]


Pauses automatic updates.



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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
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
<li>The managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.</li>
</ul>
</td>
</tr>
</table>

## -remarks

This method requires administrator permissions.

Automatic Updates can be paused for only eight hours.  This limit  varies in different binary versions. 
    Callers should call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-resume">Resume</a> method after 
    calling <b>Pause</b> as soon as they no longer need to 
    pause automatic updating.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the 
    interface is locked down.

This method returns <b>WU_E_AU_NOSERVICE</b> if Automatic Updates is disabled, 
    initializing, uninitializing, or not configured.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">IAutomaticUpdates</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-resume">IAutomaticUpdates.Resume</a>
