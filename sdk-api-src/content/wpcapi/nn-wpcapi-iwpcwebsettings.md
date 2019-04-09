---
UID: NN:wpcapi.IWPCWebSettings
title: IWPCWebSettings (wpcapi.h)
author: windows-sdk-content
description: Accesses web restrictions settings for the user.
old-location: parcon\iwpcwebsettings.htm
tech.root: parcon
ms.assetid: 80629db8-0040-4545-a313-5cf7aa3d7f8b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWPCWebSettings, IWPCWebSettings interface, IWPCWebSettings interface,described, parcon.iwpcwebsettings, wpcapi/IWPCWebSettings
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
 - IWPCWebSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWPCWebSettings interface


## -description


Accesses web restrictions settings for the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCWebSettings</b> interface inherits from <b>IWPCSettings</b>. <b>IWPCWebSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCWebSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf0c1a54-ac36-45f4-8005-1847dc00bf7f">GetSettings</a>
</td>
<td align="left" width="63%">
Retrieves the web restrictions settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e229b0e-59ae-4fcf-a398-32bc20611802">RequestURLOverride</a>
</td>
<td align="left" width="63%">
Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state.

</td>
</tr>
</table> 

