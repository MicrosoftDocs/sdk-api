---
UID: NN:wmprealestate.IWMPNodeWindowed
title: IWMPNodeWindowed
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK. The IWMPNodeWindowed interface is implemented by the plug-in.
old-location: wmp\iwmpnodewindowed__deprecated.htm
old-project: WMP
ms.assetid: ef99ff7c-d4b0-448e-8057-037535aaf847
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeWindowed, IWMPNodeWindowed (deprecated), IWMPNodeWindowed (deprecated) interface [Windows Media Player], IWMPNodeWindowed (deprecated) interface [Windows Media Player],described, IWMPNodeWindowedInterfaceRendering, wmp.iwmpnodewindowed__deprecated, wmprealestate/IWMPNodeWindowed (deprecated)
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
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
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmprealestate.h
api_name:
-	IWMPNodeWindowed (deprecated)
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeWindowed interface


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        

The <b>IWMPNodeWindowed</b> interface is implemented by the plug-in.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPNodeWindowed (deprecated)</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPNodeWindowed (deprecated)</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPNodeWindowed (deprecated)</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d42bdb97-6821-4e4a-b98d-ed03f978b5c1">GetOwnerWindow (deprecated)</a>
</td>
<td align="left" width="63%">
Returns the window handle previously set by Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33541e65-57dc-488a-ab34-6ac2e5ecda58">SetOwnerWindow (deprecated)</a>
</td>
<td align="left" width="63%">
Receives a handle to the window the plug-in will use for rendering.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a451a4e8-98df-4b53-8bdd-1bcc7e3437c0">Rendering Plug-ins Interfaces (deprecated)</a>
 

 

