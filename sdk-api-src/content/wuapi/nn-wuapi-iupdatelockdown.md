---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUpdateLockdown interface


## -description


Restricts access to methods and properties of objects that implements the method of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateLockdown</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUpdateLockdown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateLockdown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt764026">Lockdown</a>
</td>
<td align="left" width="63%">
Restricts access to the methods and properties of the object that implements this method.

</td>
</tr>
</table> 


## -remarks



The <b>IUpdateLockdown</b> interface is derived from <a href="_com_iunknown">IUnknown</a>, not <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. It cannot be accessed by using a script. This interface restricts access to the Windows Update  website.

The following classes implement the <b>IUpdateLockdown</b> interface:



<ul>
<li>AutomaticUpdates</li>
<li>UpdateDownloader</li>
<li>UpdateInstaller</li>
<li>UpdateServiceManager</li>
<li>WebProxy</li>
</ul>


