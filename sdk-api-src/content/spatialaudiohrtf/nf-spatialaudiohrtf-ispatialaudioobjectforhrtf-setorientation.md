---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetOrientation
title: ISpatialAudioObjectForHrtf::SetOrientation
author: windows-sdk-content
description: Sets the orientation in 3D space, relative to the listener's frame of reference, from which the ISpatialAudioObjectForHrtf audio data will be rendered.
old-location: coreaudio\ispatialaudioobjectforhrtf_setorientation.htm
tech.root: CoreAudio
ms.assetid: 2B88643A-C81A-4F11-BFD0-EEF4C65861C8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetOrientation method, ISpatialAudioObjectForHrtf.SetOrientation, ISpatialAudioObjectForHrtf::SetOrientation, SetOrientation, SetOrientation method [Core Audio], SetOrientation method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setorientation, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetOrientation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudiohrtf.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectForHrtf.SetOrientation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectForHrtf::SetOrientation


## -description


Sets the orientation in 3D space, relative to the listener's frame of reference, from which the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> audio data will be rendered.


## -parameters




### -param orientation [in]

An array of floats defining row-major 3x3 rotation matrix.


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
<dt><b>SPTLAUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetOrientation</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/82AA5202-C12C-4DFB-B4C5-745D4756C1FA">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/76E52F77-C0BA-4237-83BC-3E687D94EE7A">ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>
 




## -remarks



If <b>SetOrientation</b> is never called, the default value of an identity matrix is used. After <b>SetOrientation</b> is called, the orientation that is set will be used for the audio object until the orientation is changed with another call to <b>SetOrientation</b>.




## -see-also




<a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>
 

 

