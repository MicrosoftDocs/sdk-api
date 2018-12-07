---
UID: NN:tuner.IDVBSTuningSpace
title: IDVBSTuningSpace
author: windows-sdk-content
description: The IDVBSTuningSpace interface is implemented on the DVBTuningSpace object and provides methods for working with tuning spaces with a DVBS network type.
old-location: mstv\idvbstuningspace.htm
tech.root: mstv
ms.assetid: 46c143d7-b9ec-4808-a4d2-337e6e0252dd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDVBSTuningSpace, IDVBSTuningSpace interface [Microsoft TV Technologies], IDVBSTuningSpace interface [Microsoft TV Technologies],described, IDVBSTuningSpaceInterface, mstv.idvbstuningspace, tuner/IDVBSTuningSpace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IDVBSTuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVBSTuningSpace interface


## -description



The <b>IDVBSTuningSpace</b> interface is implemented on the <b>DVBTuningSpace</b> object and provides methods for working with tuning spaces with a DVBS network type.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBSTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/01325520-0cb3-46c2-b5a1-f07c5f8d7c7b">IDVBTuningSpace2</a>. <b>IDVBSTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBSTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3b70684-5066-411e-9946-ccfc1efa3e7c">get_HighOscillator</a>
</td>
<td align="left" width="63%">
Retrieves the high oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d116c1d1-df48-434b-ad49-eabd0efaa810">get_InputRange</a>
</td>
<td align="left" width="63%">
Retrieves an integer indicating which option or switch contains the requested signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56cea4ef-7679-4b78-883d-194c9259032f">get_LNBSwitch</a>
</td>
<td align="left" width="63%">
Retrieves the LNB switch frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f48902d-9242-4791-b0f1-fc4ab5bd85c0">get_LowOscillator</a>
</td>
<td align="left" width="63%">
Retrieves the low oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68374808-2999-4196-9b2b-b6c97308b041">get_SpectralInversion</a>
</td>
<td align="left" width="63%">
Retrieves an integer indicating the spectral inversion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f71008b-dbb6-485b-b196-7c2d215b3064">put_HighOscillator</a>
</td>
<td align="left" width="63%">
Sets the high oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa7c065e-91c7-4780-a33a-c5f6bf77a2c4">put_InputRange</a>
</td>
<td align="left" width="63%">
Sets an integer indicating which option or switch contains the requested signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f9ae9e-ba0d-468d-81c2-4641770e39a5">put_LNBSwitch</a>
</td>
<td align="left" width="63%">
Sets the LNB switch frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cadc2818-d54c-410a-9894-28baa51b9b01">put_LowOscillator</a>
</td>
<td align="left" width="63%">
Sets the low oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3fd3237-6c10-419d-b1ce-7cb00ebb3442">put_SpectralInversion</a>
</td>
<td align="left" width="63%">
Sets an integer indicating the spectral inversion.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBSTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/01325520-0cb3-46c2-b5a1-f07c5f8d7c7b">IDVBTuningSpace2</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

