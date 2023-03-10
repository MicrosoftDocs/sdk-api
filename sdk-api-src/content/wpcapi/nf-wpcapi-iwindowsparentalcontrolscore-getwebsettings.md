---
UID: NF:wpcapi.IWindowsParentalControlsCore.GetWebSettings
title: IWindowsParentalControlsCore::GetWebSettings (wpcapi.h)
description: Retrieves a pointer to an interface for web restrictions settings for the specified user.
helpviewer_keywords: ["GetWebSettings","GetWebSettings method","GetWebSettings method","IWindowsParentalControlsCore interface","IWindowsParentalControlsCore interface","GetWebSettings method","IWindowsParentalControlsCore.GetWebSettings","IWindowsParentalControlsCore::GetWebSettings","parcon.iwindowsparentalcontrols_getwebsettings","wpcapi/IWindowsParentalControlsCore::GetWebSettings"]
old-location: parcon\iwindowsparentalcontrols_getwebsettings.htm
tech.root: parcon
ms.assetid: ed01e945-06e7-4d3d-8a23-066ef6e0b13c
ms.date: 12/05/2018
ms.keywords: GetWebSettings, GetWebSettings method, GetWebSettings method,IWindowsParentalControlsCore interface, IWindowsParentalControlsCore interface,GetWebSettings method, IWindowsParentalControlsCore.GetWebSettings, IWindowsParentalControlsCore::GetWebSettings, parcon.iwindowsparentalcontrols_getwebsettings, wpcapi/IWindowsParentalControlsCore::GetWebSettings
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
 - IWindowsParentalControlsCore::GetWebSettings
 - wpcapi/IWindowsParentalControlsCore::GetWebSettings
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
 - IWindowsParentalControlsCore.GetWebSettings
---

# IWindowsParentalControlsCore::GetWebSettings


## -description

Retrieves a pointer to an interface for web restrictions settings for the specified user.

## -parameters

### -param pcszSID [in]

The SID string of the user. If this parameter is <b>NULL</b>, retrieve settings for the current user.

### -param ppSettings [out]

A pointer to an <a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcwebsettings">IWPCWebSettings</a> interface pointer.

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



<a href="nn-wpcapi-iwindowsparentalcontrolscore.md">IWindowsParentalControlsCore</a>