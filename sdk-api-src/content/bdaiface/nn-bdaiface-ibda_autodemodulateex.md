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

# IBDA_AutoDemodulateEx interface


## -description



The <b>IBDA_AutoDemodulateEx</b> interface extends <a href="https://msdn.microsoft.com/91588290-bae9-4c6d-9ec7-5d3777208e2a">IBDA_AutoDemodulate</a>. If a BDA device filter, specifically a demodulator, exposes this interface, it indicates that the filter can automatically detect signal characteristics. With this information, the Network Provider can be more efficient in managing the tuning process. For more information, see <b>KSPROPSETID_BdaAutodemodulate</b> in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_AutoDemodulateEx</b> interface inherits from <a href="https://msdn.microsoft.com/91588290-bae9-4c6d-9ec7-5d3777208e2a">IBDA_AutoDemodulate</a>. <b>IBDA_AutoDemodulateEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_AutoDemodulateEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a23a1d54-377e-48cb-a4ff-dfd5a6972677">get_AuxInputCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of the number of auxiliary inputs on the demodulator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94d105f5-a609-4c10-b63e-61e39ee66fd3">get_SupportedDeviceNodeTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of the device node types that the demodulator supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bba4a57c-7e07-45ca-84d0-921caf39f345">get_SupportedVideoFormats</a>
</td>
<td align="left" width="63%">
Retrieves the video formats that are supported by the demodulator.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_AutoDemodulateEx)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/91588290-bae9-4c6d-9ec7-5d3777208e2a">IBDA_AutoDemodulate</a>
 

 

