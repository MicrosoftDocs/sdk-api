---
UID: NN:tuner.IDigitalCableTuningSpace
title: IDigitalCableTuningSpace
author: windows-sdk-content
description: The IDigitalCableTuningSpace interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.
old-location: mstv\idigitalcabletuningspace.htm
old-project: mstv
ms.assetid: a0788405-5502-4d6a-8f94-9957859ac1af
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDigitalCableTuningSpace, IDigitalCableTuningSpace interface [Microsoft TV Technologies], IDigitalCableTuningSpace interface [Microsoft TV Technologies],described, IDigitalCableTuningSpaceInterface, mstv.idigitalcabletuningspace, tuner/IDigitalCableTuningSpace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDigitalCableTuningSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDigitalCableTuningSpace interface


## -description



The <b>IDigitalCableTuningSpace</b> interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDigitalCableTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace</a>. <b>IDigitalCableTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDigitalCableTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00910dbb-3265-4e90-a5c5-110d7648e161">get_MaxMajorChannel</a>
</td>
<td align="left" width="63%">
Retrieves the highest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f408777-11a0-4c86-95e6-9bfe7c917bb3">get_MaxSourceID</a>
</td>
<td align="left" width="63%">
Retrieves the highest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa7df820-c970-4333-b4e3-54d68d951f1e">get_MinMajorChannel</a>
</td>
<td align="left" width="63%">
Retrieves the lowest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54123d08-e01c-466e-833f-8412e06ac139">get_MinSourceID</a>
</td>
<td align="left" width="63%">
Retrieves the lowest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbe0add4-dc2e-4d0b-9d78-a67ce75edba0">put_MaxMajorChannel</a>
</td>
<td align="left" width="63%">
Sets the highest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e81caac5-8494-43af-bdca-9894efb90765">put_MaxSourceID</a>
</td>
<td align="left" width="63%">
Sets the highest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b5e1a01-5471-4bf4-9f08-ce910c69ba26">put_MinMajorChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99dd4964-a19f-4f68-bc4a-e4d5c558cb82">put_MinSourceID</a>
</td>
<td align="left" width="63%">
Sets the lowest source identifier for this tuning space.

</td>
</tr>
</table> 


## -remarks




        To set minimum and maximum values for the virtual channel number, use the <a href="https://msdn.microsoft.com/e0e348a6-a536-4c1b-82ba-c2502c5d92c0">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="https://msdn.microsoft.com/2a559069-0d8a-4904-b0de-0573b4c0d273">IAnalogTVTuningSpace::put_MaxChannel</a> methods. (This interface inherits <a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace</a> through <a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace</a>.)
      


        To set minimum and maximum values for the minor channel number, use the <a href="https://msdn.microsoft.com/71ae8be2-8e80-49ff-9d1b-be42a620c20c">IATSCTuningSpace::put_MinMinorChannel</a> and <a href="https://msdn.microsoft.com/e90b78da-abd5-40bc-8d88-8a257acabe23">IATSCTuningSpace::put_MaxMinorChannel</a> methods.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDigitalCableTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

