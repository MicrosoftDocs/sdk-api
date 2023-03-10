---
UID: NF:endpointvolume.IAudioEndpointVolume.QueryHardwareSupport
title: IAudioEndpointVolume::QueryHardwareSupport (endpointvolume.h)
description: The QueryHardwareSupport method queries the audio endpoint device for its hardware-supported functions. (IAudioEndpointVolume.QueryHardwareSupport)
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","QueryHardwareSupport method","IAudioEndpointVolume.QueryHardwareSupport","IAudioEndpointVolume::QueryHardwareSupport","IAudioEndpointVolumeQueryHardwareSupport","QueryHardwareSupport","QueryHardwareSupport method [Core Audio]","QueryHardwareSupport method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_queryhardwaresupport","endpointvolume/IAudioEndpointVolume::QueryHardwareSupport"]
old-location: coreaudio\iaudioendpointvolume_queryhardwaresupport.htm
tech.root: CoreAudio
ms.assetid: 20d04cff-f101-417e-912f-c87af16184db
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],QueryHardwareSupport method, IAudioEndpointVolume.QueryHardwareSupport, IAudioEndpointVolume::QueryHardwareSupport, IAudioEndpointVolumeQueryHardwareSupport, QueryHardwareSupport, QueryHardwareSupport method [Core Audio], QueryHardwareSupport method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_queryhardwaresupport, endpointvolume/IAudioEndpointVolume::QueryHardwareSupport
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointVolume::QueryHardwareSupport
 - endpointvolume/IAudioEndpointVolume::QueryHardwareSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.QueryHardwareSupport
---

# IAudioEndpointVolume::QueryHardwareSupport


## -description

The <i>QueryHardwareSupport</i> method queries the audio endpoint device for its hardware-supported functions.

## -parameters

### -param pdwHardwareSupportMask [out]

Pointer to a <b>DWORD</b> variable into which the method writes a hardware support mask that indicates the hardware capabilities of the audio endpoint device. The method can set the mask to 0 or to the bitwise-OR combination of one or more <a href="/windows/desktop/CoreAudio/endpoint-hardware-support-xxx-constants">ENDPOINT_HARDWARE_SUPPORT_XXX</a> constants.

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
The system automatically substitutes a software implementation for any function in the preceding list that the endpoint device does not implement in hardware.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>
