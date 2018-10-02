---
UID: NN:wpcapi.IWPCSettings
title: IWPCSettings
author: windows-sdk-content
description: Accesses general settings for the user.
old-location: parcon\iwpcsettings.htm
tech.root: parcon
ms.assetid: 92ae8611-fbb4-470e-8a48-395defaef904
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWPCSettings, IWPCSettings interface, IWPCSettings interface,described, parcon.iwpcsettings, wpcapi/IWPCSettings
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
 - IWPCSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWPCSettings interface


## -description


Accesses general settings for the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWPCSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fe5be0c-e6fa-481d-a28d-c5b15257b901">GetLastSettingsChangeTime</a>
</td>
<td align="left" width="63%">
Retrieves the time at which the configuration settings were last updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22350ef3-3068-4d33-a023-74644e5fbb83">GetRestrictions</a>
</td>
<td align="left" width="63%">
Determines whether web restrictions, time limits, or game restrictions are on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfe04843-af23-4146-bc45-f91d6ad36c1a">IsLoggingRequired</a>
</td>
<td align="left" width="63%">
Determines whether activity logging should be performed when obtaining the <b>IWPCSettings</b> interface.

</td>
</tr>
</table> 

