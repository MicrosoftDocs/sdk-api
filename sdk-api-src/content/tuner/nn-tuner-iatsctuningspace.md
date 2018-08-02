---
UID: NN:tuner.IATSCTuningSpace
title: IATSCTuningSpace
author: windows-sdk-content
description: The IATSCTuningSpace interface is implemented on ATSCTuningSpace objects, which represent any tuning space with an ATSC network type.
old-location: mstv\iatsctuningspace.htm
old-project: mstv
ms.assetid: 313508e5-a9b2-42b8-bb2f-d191944d0939
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IATSCTuningSpace, IATSCTuningSpace interface [Microsoft TV Technologies], IATSCTuningSpace interface [Microsoft TV Technologies],described, IATSCTuningSpaceInterface, mstv.iatsctuningspace, tuner/IATSCTuningSpace
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCTuningSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCTuningSpace interface


## -description



The <b>IATSCTuningSpace</b> interface is implemented on <a href="https://msdn.microsoft.com/8535a8c3-35df-4c6c-872a-437f5c7a2e56">ATSCTuningSpace</a> objects, which represent any tuning space with an ATSC network type. Microsoft provides a default ATSC tuning space with Windows XP, and also with DirectX 9.0. Third parties such as cable providers may install a custom tuning space using the <a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer</a> interface. An ATSCTuningSpace object creates tune requests that expose <a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace</a>. <b>IATSCTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55bfef31-f9c2-4edb-b4a9-369424584316">get_MaxMinorChannel</a>
</td>
<td align="left" width="63%">
Gets the highest minor channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42aeab8d-f05c-423d-bd35-ac030adc6434">get_MaxPhysicalChannel</a>
</td>
<td align="left" width="63%">
Gets the highest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93068602-0efa-45f2-9883-d8b681cd3a0f">get_MinMinorChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest minor channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b85331a-d99f-4cb6-8440-1b51fa697ade">get_MinPhysicalChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e90b78da-abd5-40bc-8d88-8a257acabe23">put_MaxMinorChannel</a>
</td>
<td align="left" width="63%">
Sets the highest minor channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/842d2c13-eef2-42d9-9642-50ec2aafb760">put_MaxPhysicalChannel</a>
</td>
<td align="left" width="63%">
Sets the highest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ae8be2-8e80-49ff-9d1b-be42a620c20c">put_MinMinorChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest minor channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57192470-8013-4812-af95-cb6ce92bea83">put_MinPhysicalChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest physical channel number ever allowed for this tuning space.

</td>
</tr>
</table> 


## -remarks



If the minimum and maximum channels are set, and the user specifies a channel that is greater than the maximum, the tuner automatically wraps around to the minimum value.

To set the minimum and maximum major channel, call <a href="https://msdn.microsoft.com/e0e348a6-a536-4c1b-82ba-c2502c5d92c0">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="https://msdn.microsoft.com/2a559069-0d8a-4904-b0de-0573b4c0d273">IAnalogTVTuningSpace::put_MaxChannel</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

