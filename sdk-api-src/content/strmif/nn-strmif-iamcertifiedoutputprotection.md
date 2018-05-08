---
UID: NN:strmif.IAMCertifiedOutputProtection
title: IAMCertifiedOutputProtection
author: windows-driver-content
description: The IAMCertifiedOutputProtection interface sends Certified Output Protection Protocol (COPP) messages to the graphics driver.
old-location: dshow\iamcertifiedoutputprotection.htm
old-project: DirectShow
ms.assetid: e5da271d-9528-4bcb-8b76-56fbec2e5855
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMCertifiedOutputProtection, IAMCertifiedOutputProtection interface [DirectShow], IAMCertifiedOutputProtection interface [DirectShow],described, IAMCertifiedOutputProtectionInterface, dshow.iamcertifiedoutputprotection, strmif/IAMCertifiedOutputProtection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMCertifiedOutputProtection
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMCertifiedOutputProtection interface


## -description



The <code>IAMCertifiedOutputProtection</code> interface sends Certified Output Protection Protocol (COPP) messages to the graphics driver. This interface is exposed by the Video Mixing Renderer 7 (VMR-7) and Video Mixing Renderer 9 (VMR-9) filters.

For information about using COPP, see <a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMCertifiedOutputProtection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMCertifiedOutputProtection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMCertifiedOutputProtection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/163164a2-e2a2-447d-b443-f92972197aff">KeyExchange</a>
</td>
<td align="left" width="63%">
Returns the graphics driver's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/facf13b2-6650-4e81-97ba-eadacc514ef0">ProtectionCommand</a>
</td>
<td align="left" width="63%">
Sends a COPP command to the graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93ebbcc-ce44-4d77-b088-7112ddaf41b2">ProtectionStatus</a>
</td>
<td align="left" width="63%">
Sends a COPP status request to the graphics driver

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0321e315-b53c-487f-a015-80f7ed581737">SessionSequenceStart</a>
</td>
<td align="left" width="63%">
Initiates the COPP session with the graphics driver.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

