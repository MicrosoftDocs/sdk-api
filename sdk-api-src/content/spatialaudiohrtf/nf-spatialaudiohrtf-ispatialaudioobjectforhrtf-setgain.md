---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetGain
title: ISpatialAudioObjectForHrtf::SetGain
author: windows-sdk-content
description: Sets the gain for the ISpatialAudioObjectForHrtf.
old-location: coreaudio\ispatialaudioobjectforhrtf_setgain.htm
old-project: CoreAudio
ms.assetid: 7DE268DC-5AA0-4866-8495-34292AEFB142
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetGain method, ISpatialAudioObjectForHrtf.SetGain, ISpatialAudioObjectForHrtf::SetGain, SetGain, SetGain method [Core Audio], SetGain method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setgain, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetGain
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectForHrtf.SetGain
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForHrtf::SetGain


## -description


Sets the gain for the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>. 


## -parameters




### -param gain [in]

The gain for the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>. 


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

<a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamForHrtf::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetGain</b>.

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



This is valid only for spatial audio objects configured to use the <a href="https://msdn.microsoft.com/EF4ACEB1-E802-4337-AA76-467BCB90D7C6">SpatialAudioHrtfDistanceDecay_CustomDecay</a> decay type. Set the decay type of an <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> object by calling <a href="https://msdn.microsoft.com/62C95E6A-C27E-4C17-91E1-D6D80172F15B">SetDistanceDecay</a>. Set the default decay type for an all objects in an HRTF render stream by setting the <b>DistanceDecay</b> field of the <a href="https://msdn.microsoft.com/6A549BFB-993A-4A20-AFAB-B38D03EAE35C">SpatialAudioHrtfActivationParams</a> passed into <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a>.

If <b>SetGain</b> is never called, the default value of 0.0 is used. After <b>SetGain</b> is called, the gain that is set will be used for the audio object until the gain is changed with another call to <b>SetGain</b>.




## -see-also




<a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>
 

 

