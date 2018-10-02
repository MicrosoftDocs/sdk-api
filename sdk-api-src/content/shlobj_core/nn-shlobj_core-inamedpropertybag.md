---
UID: NN:shlobj_core.INamedPropertyBag
title: INamedPropertyBag
author: windows-sdk-content
description: Exposes methods that provide an object with a specified property bag in which the object can save its properties.
old-location: shell\INamedPropertyBag.htm
tech.root: Shell
ms.assetid: 5a7d6e06-712b-4b18-baad-f4166163c50f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: INamedPropertyBag, INamedPropertyBag interface [Windows Shell], INamedPropertyBag interface [Windows Shell],described, _shell_INamedPropertyBag, shell.INamedPropertyBag, shlobj_core/INamedPropertyBag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INamedPropertyBag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamedPropertyBag interface


## -description


Exposes methods that provide an object with a specified property bag in which the object can save its properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedPropertyBag</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INamedPropertyBag</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamedPropertyBag</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7080edeb-4908-4b0a-9416-9b301c54bb4c">ReadPropertyNPB</a>
</td>
<td align="left" width="63%">
Causes a property to be read from the named property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/632bab32-c546-4f8f-b064-877e853c215c">RemovePropertyNPB</a>
</td>
<td align="left" width="63%">
Removes a property from a named property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f91764ee-85eb-47ec-b983-49ec410b8c2c">WritePropertyNPB</a>
</td>
<td align="left" width="63%">
Saves a property to the named property bag.

</td>
</tr>
</table> 

