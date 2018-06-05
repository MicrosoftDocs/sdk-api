---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetDirectivity
title: ISpatialAudioObjectForHrtf::SetDirectivity
author: windows-sdk-content
description: Sets the spatial audio directivity model for the ISpatialAudioObjectForHrtf.
old-location: coreaudio\ispatialaudioobjectforhrtf_setdirectivity.htm
old-project: CoreAudio
ms.assetid: 20934FA5-2B4E-4FC4-B5B5-AFC4024ED2F8
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetDirectivity method, ISpatialAudioObjectForHrtf.SetDirectivity, ISpatialAudioObjectForHrtf::SetDirectivity, SetDirectivity, SetDirectivity method [Core Audio], SetDirectivity method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setdirectivity, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDirectivity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SpatialAudioHrtfEnvironmentType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudiohrtf.h
api_name:
-	ISpatialAudioObjectForHrtf.SetDirectivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForHrtf::SetDirectivity


## -description


Sets the spatial audio directivity model for the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>.


## -parameters




### -param directivity

The spatial audio directivity model. This value can be one of the following structures:

<ul>
<li>
<a href="https://msdn.microsoft.com/A3D149E0-F2C1-47C7-8858-35C5F51C7F75">SpatialAudioHrtfDirectivity</a>
</li>
<li>
<a href="https://msdn.microsoft.com/71E2E152-14DC-472B-B582-82D4412EAA85">SpatialAudioHrtfDirectivityCardioid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C34F26C2-4979-4C06-8EAC-64547745238F">SpatialAudioHrtfDirectivityCone</a>
</li>
</ul>

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

<a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamForHrtf::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetDirectivity</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/82AA5202-C12C-4DFB-B4C5-745D4756C1FA">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamForHrtf::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/76E52F77-C0BA-4237-83BC-3E687D94EE7A">ISpatialAudioObjectRenderStreamForHrtf::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/A3D149E0-F2C1-47C7-8858-35C5F51C7F75">SpatialAudioHrtfDirectivity</a> structure represents an omnidirectional model that can be linearly interpolated with a cardioid or cone model.

If <b>SetDirectivity</b> is not called, the default type of <a href="https://msdn.microsoft.com/3A1426B5-F4FF-4CF0-9E0A-3096371B3D2E">SpatialAudioHrtfDirectivity_OmniDirectional</a> is used with no interpolation.




## -see-also




<a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>
 

 

