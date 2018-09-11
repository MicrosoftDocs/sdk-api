---
UID: NN:bdaiface.IBDA_Encoder
title: IBDA_Encoder
author: windows-sdk-content
description: Provides access to a device's Encoder Service.
old-location: mstv\ibda_encoder.htm
tech.root: mstv
ms.assetid: 43ed9d91-c769-4fb3-bcd9-e5239ec5d9c7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_Encoder, IBDA_Encoder interface [Microsoft TV Technologies], IBDA_Encoder interface [Microsoft TV Technologies],described, bdaiface/IBDA_Encoder, mstv.ibda_encoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_Encoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Encoder interface


## -description


Provides access to a device's Encoder Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_Encoder</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBDA_Encoder</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBDA_Encoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693324(v=VS.85).aspx">EnumAudioCapability</a>
</td>
<td align="left" width="63%">
Gets one of the audio formats supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693325(v=VS.85).aspx">EnumVideoCapability</a>
</td>
<td align="left" width="63%">
Gets one of the video formats supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693326(v=VS.85).aspx">GetState</a>
</td>
<td align="left" width="63%">
Queries the current state of the Encoder Service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693327(v=VS.85).aspx">QueryCapabilities</a>
</td>
<td align="left" width="63%">
Gets the number of encoding formats supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693328(v=VS.85).aspx">SetParameters</a>
</td>
<td align="left" width="63%">
Sets the parameters for the Encoder Service.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_Encoder)</code>.



