---
UID: NN:tuner.IATSCLocator
title: IATSCLocator
author: windows-sdk-content
description: The IATSCLocator interface is implemented on the ATSCLocator object and contains methods that enable the network provider to determine the physical channel and transport stream ID of an ATSC transmission.
old-location: mstv\iatsclocator.htm
tech.root: MSTV
ms.assetid: 8ca7d50f-e7cc-4938-a2ed-fce5278b73fd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IATSCLocator, IATSCLocator interface [Microsoft TV Technologies], IATSCLocator interface [Microsoft TV Technologies],described, IATSCLocatorInterface, mstv.iatsclocator, tuner/IATSCLocator
ms.prod: windows
ms.technology: windows-sdk
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
 - IATSCLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSCLocator interface


## -description



The <b>IATSCLocator</b> interface is implemented on the <a href="https://msdn.microsoft.com/5fe75e72-1feb-4e30-a7f5-cf29a6c9f201">ATSCLocator</a> object and contains methods that enable the network provider to determine the physical channel and transport stream ID of an ATSC transmission. Applications do not use Locator interfaces except possibly for debugging purposes. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCLocator</b> interface inherits from <a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>. <b>IATSCLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7550bbb9-d9f7-4565-9c63-7179c0bdffa5">get_PhysicalChannel</a>
</td>
<td align="left" width="63%">
Retrieves the physical channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7cde550-742c-426c-a350-1d05b74f824d">get_TSID</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0699e4ef-7ebb-4515-9894-1592f07607ed">put_PhysicalChannel</a>
</td>
<td align="left" width="63%">
Sets the physical channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1864d2e7-0d4a-44b6-a9db-11f6efcd6986">put_TSID</a>
</td>
<td align="left" width="63%">
Sets the transport stream ID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCLocator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

