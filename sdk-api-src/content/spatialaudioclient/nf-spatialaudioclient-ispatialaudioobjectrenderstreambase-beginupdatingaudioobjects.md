---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects
title: ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects
author: windows-sdk-content
description: Puts the system into the state where audio object data can be submitted for processing and the ISpatialAudioObject state can be modified.
old-location: coreaudio\ispatialaudioobjectrenderstream_beginupdatingaudioobjects.htm
tech.root: CoreAudio
ms.assetid: 9D858556-2EBE-4DF6-878B-BE0E12079248
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: BeginUpdatingAudioObjects, BeginUpdatingAudioObjects method [Core Audio], BeginUpdatingAudioObjects method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],BeginUpdatingAudioObjects method, ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects, ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects, coreaudio.ispatialaudioobjectrenderstream_beginupdatingaudioobjects, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- spatialaudioclient.h
: 
- ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects
: 
---

# ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects


## -description


Puts the system into the state where audio object data can be submitted for processing and the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> state can be modified.


## -parameters




### -param availableDynamicObjectCount [out]

The number of dynamic audio objects that are available to be rendered for the current processing pass. All allocated static audio objects can be rendered in every pass. For information on audio object types, see <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a>.


### -param frameCountPerBuffer [out]

The size, in audio frames, of the buffer returned by <a href="https://msdn.microsoft.com/CD777E2D-4CA0-4C2D-A475-22BF770DD59D">GetBuffer</a>.


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
<b>BeginUpdatingAudioObjects</b> was called twice without a matching call to <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">EndUpdatingAudioObjects</a> between the two calls.

</td>
</tr>
</table>
 




## -remarks



This method must be called each time the event passed in the <a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a> to <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> is signaled,  
     even if there no audio object data to submit.

For each <b>BeginUpdatingAudioObjects</b> call, there should be a corresponding call to <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">EndUpdatingAudioObjects</a> call.  
    If <b>BeginUpdatingAudioObjects</b> is called twice without a call <b>EndUpdatingAudioObjects</b> between them, the second call to  
    <b>BeginUpdatingAudioObjects</b> will return SPTLAUDCLNT_E_OUT_OF_ORDER.




## -see-also




<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a>
 

 

