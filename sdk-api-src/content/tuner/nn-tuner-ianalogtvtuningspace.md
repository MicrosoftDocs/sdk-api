---
UID: NN:tuner.IAnalogTVTuningSpace
title: IAnalogTVTuningSpace
author: windows-sdk-content
description: The IAnalogTVTuningSpace interface provides methods for getting and setting parameters associated with analog TV tuning spaces. The Video Control uses these methods when building and controlling a WDM Analog TV filter graph.
old-location: mstv\ianalogtvtuningspace.htm
tech.root: mstv
ms.assetid: 2b531f09-bf2e-4eb2-abcf-60f64cbee17b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAnalogTVTuningSpace, IAnalogTVTuningSpace interface [Microsoft TV Technologies], IAnalogTVTuningSpace interface [Microsoft TV Technologies],described, IAnalogTVTuningSpaceInterface, mstv.ianalogtvtuningspace, tuner/IAnalogTVTuningSpace
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
 - IAnalogTVTuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAnalogTVTuningSpace interface


## -description



The <b>IAnalogTVTuningSpace</b> interface provides methods for getting and setting parameters associated with analog TV tuning spaces. The Video Control uses these methods when building and controlling a WDM Analog TV filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogTVTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>. <b>IAnalogTVTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogTVTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f74f31cc-8e3a-41b8-bf27-f60b9cbcfcdb">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c016a61b-6b4f-4101-a357-38b8be754a57">get_InputType</a>
</td>
<td align="left" width="63%">
Gets the input type (antenna or cable) intended for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6ac3789-1989-4331-ad00-6720f4503bb7">get_MaxChannel</a>
</td>
<td align="left" width="63%">
Gets the highest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94c3136f-6d9e-4396-9bbf-828669d57724">get_MinChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb53bdfe-6293-41f3-8945-5f960193df9e">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399503a2-60e9-4feb-ba69-cafef70b2540">put_InputType</a>
</td>
<td align="left" width="63%">
Sets the input type (antenna or cable) intended for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a559069-0d8a-4904-b0de-0573b4c0d273">put_MaxChannel</a>
</td>
<td align="left" width="63%">
Sets the highest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e348a6-a536-4c1b-82ba-c2502c5d92c0">put_MinChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest channel number for this tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogTVTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

