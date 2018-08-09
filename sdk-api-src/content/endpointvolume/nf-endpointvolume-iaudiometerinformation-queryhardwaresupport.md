---
UID: NF:endpointvolume.IAudioMeterInformation.QueryHardwareSupport
title: IAudioMeterInformation::QueryHardwareSupport
author: windows-sdk-content
description: The QueryHardwareSupport method queries the audio endpoint device for its hardware-supported functions.
old-location: coreaudio\iaudiometerinformation_queryhardwaresupport.htm
old-project: CoreAudio
ms.assetid: 3f68a459-8c10-46f5-be5c-67b693d65b8b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAudioMeterInformation interface [Core Audio],QueryHardwareSupport method, IAudioMeterInformation.QueryHardwareSupport, IAudioMeterInformation::QueryHardwareSupport, IAudioMeterInformationQueryHardwareSupport, QueryHardwareSupport, QueryHardwareSupport method [Core Audio], QueryHardwareSupport method [Core Audio],IAudioMeterInformation interface, coreaudio.iaudiometerinformation_queryhardwaresupport, endpointvolume/IAudioMeterInformation::QueryHardwareSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioMeterInformation.QueryHardwareSupport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioMeterInformation::QueryHardwareSupport


## -description



The <b>QueryHardwareSupport</b> method queries the audio endpoint device for its hardware-supported functions.




## -parameters




### -param pdwHardwareSupportMask [out]

Pointer to a <b>DWORD</b> variable into which the method writes a hardware support mask that indicates the hardware capabilities of the audio endpoint device. The method can set the mask to 0 or to the bitwise-OR combination of one or more <a href="https://msdn.microsoft.com/54032f75-2287-4589-bda5-e005ee077c41">ENDPOINT_HARDWARE_SUPPORT_XXX</a> constants.


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
Parameter <i>pdwHardwareSupportMask</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method indicates whether the audio endpoint device implements the following functions in hardware:

<ul>
<li>Volume control</li>
<li>Mute control</li>
<li>Peak meter</li>
</ul>
The system automatically substitutes a software implementation for any function in the preceding list that the endpoint devices does not implement in hardware.




## -see-also




<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation Interface</a>
 

 

