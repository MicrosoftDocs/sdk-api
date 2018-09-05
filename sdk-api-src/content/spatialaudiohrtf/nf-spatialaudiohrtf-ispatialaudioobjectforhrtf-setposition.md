---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetPosition
title: ISpatialAudioObjectForHrtf::SetPosition
author: windows-sdk-content
description: Sets the position in 3D space, relative to the listener, from which the ISpatialAudioObjectForHrtf audio data will be rendered.
old-location: coreaudio\ispatialaudioobjectforhrtf_setposition.htm
old-project: CoreAudio
ms.assetid: 4FB6852D-A793-43A1-A58F-E7DCFDB5BBDD
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetPosition method, ISpatialAudioObjectForHrtf.SetPosition, ISpatialAudioObjectForHrtf::SetPosition, SetPosition, SetPosition method [Core Audio], SetPosition method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setposition, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetPosition
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
 - ISpatialAudioObjectForHrtf.SetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForHrtf::SetPosition


## -description


Sets the position in 3D space, relative to the listener, from which the <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> audio data will be rendered.


## -parameters




### -param x [in]

The x position of the audio object, in meters, relative to the listener. Positive values are to the right of the listener and negative values are to the left.


### -param y [in]

The y position of the audio object, in meters, relative to the listener. Positive values are above the listener and negative values are below.


### -param z [in]

The z position of the audio object, in meters, relative to the listener. Positive values are behind the listener and negative values are in front.


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

<a href="https://msdn.microsoft.com/3852592F-2160-46A1-AC98-3B39A32E80AF">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetPosition</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b> SPTLAUDCLNT_E_PROPERTY_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> is not of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/3E26D14B-5F69-4EBD-A48D-D63E24520D59">ISpatialAudioObjectRenderStreamBase::ActivateSpatialAudioObjectForHrtf</a> method.

</td>
</tr>
</table>
 




## -remarks



This method can only be called on a  <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> that is of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/3E26D14B-5F69-4EBD-A48D-D63E24520D59">ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf</a> method.

 Position values use a right-handed Cartesian coordinate system, where each unit represents 1 meter. The coordinate system is relative to the listener where the origin (x=0.0, y=0.0, z=0.0) represents the center point between the listener's ears.

If <b>SetPosition</b> is never called, the origin (x=0.0, y=0.0, z=0.0) is used as the default position. After <b>SetPosition</b> is called, the position that is set will be used for the audio object until the position is changed with another call to <b>SetPosition</b>.




## -see-also




<a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a>
 

 

