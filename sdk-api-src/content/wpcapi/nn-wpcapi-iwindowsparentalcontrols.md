---
UID: NN:wpcapi.IWindowsParentalControls
title: IWindowsParentalControls (wpcapi.h)
author: windows-sdk-content
description: Enables access to all settings interfaces of the Minimum Compliance API.
old-location: parcon\iwindowsparentalcontrols.htm
tech.root: parcon
ms.assetid: f825388f-c4de-4bf2-8076-6efd81b6e030
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWindowsParentalControls, IWindowsParentalControls interface, IWindowsParentalControls interface,described, parcon.iwindowsparentalcontrols, wpcapi/IWindowsParentalControls
ms.topic: interface
f1_keywords: 
 - "wpcapi/IWindowsParentalControls"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWindowsParentalControls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsParentalControls interface


## -description


Enables access to all settings interfaces of the Minimum Compliance API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsParentalControls</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Mt847165(v=VS.85).aspx">IWindowsParentalControlsCore</a>. <b>IWindowsParentalControls</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsParentalControls</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwindowsparentalcontrols-getgamessettings">GetGamesSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for games restrictions settings for the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwindowsparentalcontrolscore-getusersettings">GetUserSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for general settings for the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwindowsparentalcontrolscore-getvisibility">GetVisibility</a>
</td>
<td align="left" width="63%">
Indicates the visibility of the Parental Controls user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwindowsparentalcontrolscore-getwebfilterinfo">GetWebFilterInfo</a>
</td>
<td align="left" width="63%">
Retrieves the name and identifier of the currently active Web Content Filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwindowsparentalcontrolscore-getwebsettings">GetWebSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for web restrictions settings for the specified user.

</td>
</tr>
</table> 

