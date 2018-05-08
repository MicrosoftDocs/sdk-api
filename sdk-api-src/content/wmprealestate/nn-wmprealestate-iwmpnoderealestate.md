---
UID: NN:wmprealestate.IWMPNodeRealEstate
title: IWMPNodeRealEstate
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK. The IWMPNodeRealEstate interface is implemented by the plug-in.
old-location: wmp\iwmpnoderealestate__deprecated.htm
old-project: WMP
ms.assetid: 0c9d382a-26de-4e53-9950-76916863f116
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeRealEstate, IWMPNodeRealEstate (deprecated), IWMPNodeRealEstate (deprecated) interface [Windows Media Player], IWMPNodeRealEstate (deprecated) interface [Windows Media Player],described, IWMPNodeRealEstateInterfaceRendering, wmp.iwmpnoderealestate__deprecated, wmprealestate/IWMPNodeRealEstate (deprecated)
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
-	IWMPNodeRealEstate (deprecated)
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate interface


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        

The <b>IWMPNodeRealEstate</b> interface is implemented by the plug-in.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPNodeRealEstate (deprecated)</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPNodeRealEstate (deprecated)</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPNodeRealEstate (deprecated)</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41a7edf3-10a3-41ac-8f79-6dc0e7f854ee">GetDesiredSize (deprecated)</a>
</td>
<td align="left" width="63%">
Returns the size of the rendering area requested by the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70e028be-c824-4e6d-858d-be1c4a4ea670">GetFullScreen (deprecated)</a>
</td>
<td align="left" width="63%">
Returns a value indicating the current rendering state of the Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bb07fe6-67cd-46da-a012-0276e31e48c9">GetRects (deprecated)</a>
</td>
<td align="left" width="63%">
Returns the three <b>RECT</b> structures previously set in the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a45969c-5eba-4493-a7a8-af69f5ad3dea">GetWindowless (deprecated)</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether the plug-in is currently rendering in windowless mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63d3363d-3104-4760-b185-fd75547a53ec">SetFullScreen (deprecated)</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether the plug-in requests full screen rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0742cef9-192b-4680-83e5-350e7024a042">SetRects (deprecated)</a>
</td>
<td align="left" width="63%">
Receives information about the rendering area provided by Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408d33f6-916f-4443-8a92-fab00c11cad4">SetWindowless (deprecated)</a>
</td>
<td align="left" width="63%">
Receives a value indicating that the plug-in should render in windowless mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a451a4e8-98df-4b53-8bdd-1bcc7e3437c0">Rendering Plug-ins Interfaces (deprecated)</a>
 

 

