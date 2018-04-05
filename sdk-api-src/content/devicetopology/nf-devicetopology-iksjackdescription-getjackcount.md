---
UID: NF:devicetopology.IKsJackDescription.GetJackCount
title: IKsJackDescription::GetJackCount method
author: windows-driver-content
description: The GetJackCount method gets the number of jacks required to connect to an audio endpoint device.
old-location: coreaudio\iksjackdescription_getjackcount.htm
old-project: CoreAudio
ms.assetid: d99ad923-2846-4d3e-bc5b-b5b737219f13
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetJackCount method [Core Audio], GetJackCount method [Core Audio], IKsJackDescription interface, GetJackCount,IKsJackDescription.GetJackCount, IKsJackDescription, IKsJackDescription interface [Core Audio], GetJackCount method, IKsJackDescription::GetJackCount, IKsJackDescriptionGetJackCount, coreaudio.iksjackdescription_getjackcount, devicetopology/IKsJackDescription::GetJackCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: ConnectorType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IKsJackDescription.GetJackCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IKsJackDescription::GetJackCount method


## -description



The <b>GetJackCount</b> method gets the number of jacks required to connect to an audio endpoint device.




## -parameters




### -param pcJacks [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of jacks associated with the connector.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pcJacks</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



An audio endpoint device that plays or records a stream that contains multiple channels might require a connection with more than one jack (physical connector).

For example, a set of surround speakers that plays a 6-channel audio stream might require three stereo jacks. In this example, the first jack transmits the channels for the front-left and front-right speakers, the second jack transmits the channels for the front-center and low-frequency-effects (subwoofer) speakers, and the third jack transmits the channels for the side-left and side-right speakers.

After calling this method to retrieve the jack count, call the <a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a> method once for each jack to obtain a description of the jack.




## -see-also




<a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription Interface</a>



<a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a>
 

 

