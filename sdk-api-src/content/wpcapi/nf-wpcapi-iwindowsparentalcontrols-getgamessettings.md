---
UID: NF:wpcapi.IWindowsParentalControls.GetGamesSettings
title: IWindowsParentalControls::GetGamesSettings (wpcapi.h)
description: Retrieves a pointer to an interface for games restrictions settings for the specified user.
helpviewer_keywords: ["GetGamesSettings","GetGamesSettings method","GetGamesSettings method","IWindowsParentalControls interface","IWindowsParentalControls interface","GetGamesSettings method","IWindowsParentalControls.GetGamesSettings","IWindowsParentalControls::GetGamesSettings","parcon.iwindowsparentalcontrols_getgamessettings","wpcapi/IWindowsParentalControls::GetGamesSettings"]
old-location: parcon\iwindowsparentalcontrols_getgamessettings.htm
tech.root: parcon
ms.assetid: 2604a53e-2a95-4edd-9fb0-8b0f7298dcc4
ms.date: 12/05/2018
ms.keywords: GetGamesSettings, GetGamesSettings method, GetGamesSettings method,IWindowsParentalControls interface, IWindowsParentalControls interface,GetGamesSettings method, IWindowsParentalControls.GetGamesSettings, IWindowsParentalControls::GetGamesSettings, parcon.iwindowsparentalcontrols_getgamessettings, wpcapi/IWindowsParentalControls::GetGamesSettings
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsParentalControls::GetGamesSettings
 - wpcapi/IWindowsParentalControls::GetGamesSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWindowsParentalControls.GetGamesSettings
---

# IWindowsParentalControls::GetGamesSettings


## -description

Retrieves a pointer to an interface for games restrictions settings for the specified user.

## -parameters

### -param pcszSID [in]

The SID string of the user. If this parameter is <b>NULL</b>, retrieve settings for the current user.

### -param ppSettings [out]

A pointer to an <a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcgamessettings">IWPCGamesSettings</a> interface pointer.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The user settings were not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwindowsparentalcontrols">IWindowsParentalControls</a>