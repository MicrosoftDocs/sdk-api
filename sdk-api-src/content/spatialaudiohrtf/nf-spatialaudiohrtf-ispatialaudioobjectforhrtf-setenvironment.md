---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetEnvironment
title: ISpatialAudioObjectForHrtf::SetEnvironment
author: windows-sdk-content
description: Sets the type of acoustic environment that is simulated when audio is processed for the ISpatialAudioObjectForHrtf.
old-location: coreaudio\ispatialaudioobjectforhrtf_setenvironment.htm
old-project: CoreAudio
ms.assetid: 6D96F854-0FAE-4B8B-9033-E2AEB471B38B
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetEnvironment method, ISpatialAudioObjectForHrtf.SetEnvironment, ISpatialAudioObjectForHrtf::SetEnvironment, SetEnvironment, SetEnvironment method [Core Audio], SetEnvironment method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setenvironment, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetEnvironment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudiohrtf.h
req.include-header: 
req.redist: 
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
 - ISpatialAudioObjectForHrtf.SetEnvironment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForHrtf::SetEnvironment


## -description


Sets the type of acoustic environment that is simulated when audio is processed for the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>.


## -parameters




### -param environment [in]

A value specifying the type of acoustic environment that is simulated when audio is processed for the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>.


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

<a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetEnvironment</b>.

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



If <b>SetEnvironment</b> is not called, the default value of <a href="https://msdn.microsoft.com/017FC8D4-2B74-4B13-AF5B-D7FFF97A7E45">SpatialAudioHrtfEnvironment_Small</a> is used.




## -see-also




<a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>
 

 

