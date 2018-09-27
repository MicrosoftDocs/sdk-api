---
UID: NN:spatialaudioclient.ISpatialAudioObjectBase
title: ISpatialAudioObjectBase
author: windows-sdk-content
description: Base interface that represents an object that provides audio data to be rendered from a position in 3D space, relative to the user.
old-location: coreaudio\ispatialaudioobjectbase.htm
tech.root: CoreAudio
ms.assetid: 54721875-D93A-4C7E-A07E-C286E1A409D3
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ISpatialAudioObjectBase, ISpatialAudioObjectBase interface [Core Audio], ISpatialAudioObjectBase interface [Core Audio],described, coreaudio.ispatialaudioobjectbase, spatialaudioclient/ISpatialAudioObjectBase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ISpatialAudioObjectBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectBase interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Base interface that represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user. Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectBase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4FB5E8B-C80A-4B4B-9162-95B463543061">GetAudioObjectType</a>
</td>
<td align="left" width="63%">
Gets a value specifying the type of audio object that is represented by the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD777E2D-4CA0-4C2D-A475-22BF770DD59D">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer that is used to supply the audio data for the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3339E021-4AC3-43CB-9306-C8D58541CA5F">IsActive</a>
</td>
<td align="left" width="63%">
Gets a boolean value indicating whether the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> is valid. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Instructs the system that the final block of audio data has been  submitted for the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> so that the object can be deactivated and it's resources reused. 

</td>
</tr>
</table> 

