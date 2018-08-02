---
UID: NN:wpcapi.IWindowsParentalControls
title: IWindowsParentalControls
author: windows-sdk-content
description: Enables access to all settings interfaces of the Minimum Compliance API.
old-location: parcon\iwindowsparentalcontrols.htm
old-project: parcon
ms.assetid: f825388f-c4de-4bf2-8076-6efd81b6e030
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWindowsParentalControls, IWindowsParentalControls interface, IWindowsParentalControls interface,described, parcon.iwindowsparentalcontrols, wpcapi/IWindowsParentalControls
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWindowsParentalControls
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/2604a53e-2a95-4edd-9fb0-8b0f7298dcc4">GetGamesSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for games restrictions settings for the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c7a138-10b8-4bdf-afea-985e203e04e4">GetUserSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for general settings for the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08217ad2-3b1e-4733-8ca2-4463ffe96516">GetVisibility</a>
</td>
<td align="left" width="63%">
Indicates the visibility of the Parental Controls user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5073f335-fe55-43db-9186-aaa675384ea3">GetWebFilterInfo</a>
</td>
<td align="left" width="63%">
Retrieves the name and identifier of the currently active Web Content Filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed01e945-06e7-4d3d-8a23-066ef6e0b13c">GetWebSettings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface for web restrictions settings for the specified user.

</td>
</tr>
</table> 

