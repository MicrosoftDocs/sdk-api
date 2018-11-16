---
UID: NN:tuner.IAnalogRadioTuningSpace2
title: IAnalogRadioTuningSpace2
author: windows-sdk-content
description: This topic applies to Windows XP Media Center Edition 2004 and later.
old-location: mstv\ianalogradiotuningspace2.htm
tech.root: mstv
ms.assetid: 66e631cb-2ae8-40b0-8ec8-3a02764284bf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAnalogRadioTuningSpace2, IAnalogRadioTuningSpace2 interface [Microsoft TV Technologies], IAnalogRadioTuningSpace2 interface [Microsoft TV Technologies],described, IAnalogRadioTuningSpace2Interface, mstv.ianalogradiotuningspace2, tuner/IAnalogRadioTuningSpace2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAnalogRadioTuningSpace2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAnalogRadioTuningSpace2 interface


## -description



This topic applies to Windows XP Media Center Edition 2004 and later.
        

The <b>IAnalogRadioTuningSpace2</b> interface provides methods for getting and setting parameters associated with tuning spaces for analog radio transmission, including the source country code.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogRadioTuningSpace2</b> interface inherits from <a href="https://msdn.microsoft.com/25cf9f31-88a9-479e-b51c-ad823cd04d2d">IAnalogRadioTuningSpace</a>. <b>IAnalogRadioTuningSpace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogRadioTuningSpace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc619247-90fc-4db0-9b46-cc81b9ae6916">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89aecae6-42c0-4130-b381-986c0327fe5d">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogRadioTuningSpace2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/25cf9f31-88a9-479e-b51c-ad823cd04d2d">IAnalogRadioTuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

