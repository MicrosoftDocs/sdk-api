---
UID: NN:devicetopology.IAudioPeakMeter
title: IAudioPeakMeter
author: windows-sdk-content
description: The IAudioPeakMeter interface provides access to a hardware peak-meter control.
old-location: coreaudio\iaudiopeakmeter.htm
old-project: CoreAudio
ms.assetid: 524d83ff-4303-448c-a070-58d17dec03ba
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioPeakMeter, IAudioPeakMeter interface [Core Audio], IAudioPeakMeter interface [Core Audio],described, coreaudio.iaudiopeakmeter, devicetopology/IAudioPeakMeter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ConnectorType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IAudioPeakMeter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioPeakMeter interface


## -description



The <b>IAudioPeakMeter</b> interface provides access to a hardware peak-meter control. The client obtains a reference to the <b>IAudioPeakMeter</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioPeakMeter. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioPeakMeter</b> interface. Only a subunit object that represents a hardware peak meter will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioPeakMeter</b> interface provides convenient access to the KSPROPERTY_AUDIO_PEAKMETER property of a subunit that has a subtype GUID value of KSNODETYPE_PEAKMETER. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioPeakMeter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioPeakMeter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioPeakMeter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/699b3689-1c3f-434e-97c5-3c5930683ad1">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5d7d941-b001-49a9-b421-a999f90ddb22">GetLevel</a>
</td>
<td align="left" width="63%">
Gets the peak level that the peak meter recorded for the specified channel since the peak level for that channel was previously read.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

