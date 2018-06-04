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

# IWMPVideoRenderConfig interface


## -description



The <b>IWMPVideoRenderConfig</b> interface provides a method that configures the enhanced video renderer (EVR) used by Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPVideoRenderConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPVideoRenderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPVideoRenderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a052aecc-b37f-4999-b484-80ee3e2392ba">put_presenterActivate</a>
</td>
<td align="left" width="63%">
Provides Windows Media Player with an activation object for a custom video presenter.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPVideoRenderConfig</b> by calling <b>QueryInterface</b> through a pointer to <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a>.
<div class="alert"><b>Note</b>  If the EVR is not installed, <b>QueryInterface</b> will fail. </div><div> </div>The EVR is installed as part of the Windows Vista operating system.

Typically, the EVR is not installed on a computer running Microsoft Windows XP. The EVR is not part of Windows XP itself, and installing Windows Media Player 11 on Windows XP does not install the EVR. In some cases, however, a computer running Windows XP might have the EVR installed. For example, installing Windows Presentation Foundation on Windows XP results in the EVR being installed as well.

An application running on Windows XP without the EVR installed cannot use the <b>IWMPVideoRenderConfig</b> interface.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

