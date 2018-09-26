---
UID: NN:spatialaudioclient.ISpatialAudioClient
title: ISpatialAudioClient
author: windows-sdk-content
description: The ISpatialAudioClient interface enables a client to create audio streams that emit audio from a position in 3D space.
old-location: coreaudio\ispatialaudioclient.htm
tech.root: CoreAudio
ms.assetid: 950778D4-79FE-4222-951F-5A456A633124
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ISpatialAudioClient, ISpatialAudioClient interface [Core Audio], ISpatialAudioClient interface [Core Audio],described, coreaudio.ispatialaudioclient, spatialaudioclient/ISpatialAudioClient
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
 - ISpatialAudioClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioClient interface


## -description


The <b>ISpatialAudioClient</b> interface enables a client to create audio streams that emit audio from a position in 3D space. This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ActivateSpatialAudioStream</a>
</td>
<td align="left" width="63%">
Activates and initializes spatial audio stream using one of the spatial audio stream activation structures.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0185D09E-0009-41BF-A0BB-3C3CE0A69BA8">GetMaxDynamicObjectCount</a>
</td>
<td align="left" width="63%">
Gets the maximum number of dynamic audio objects for the spatial audio client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA28103B-6C9C-46C8-9C21-73573B42DDC4">GetMaxFrameCount</a>
</td>
<td align="left" width="63%">
Gets the maximum possible frame count per processing pass. This method can be used to determine the size of the source buffer that should be allocated to convey audio data for each processing pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29963682-AD45-4CEC-81A0-4B834505F9D5">GetNativeStaticObjectTypeMask</a>
</td>
<td align="left" width="63%">
Gets a  channel mask which represents the subset of static speaker bed channels native to current rendering engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8CD558A-994D-46E0-98A0-1D7AD3B919C0">GetStaticObjectPosition</a>
</td>
<td align="left" width="63%">
Gets the position in 3D space of the specified static spatial audio channel. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB152D8C-DE3A-4224-A6CC-DF1BFF1A3ABA">GetSupportedAudioObjectFormatEnumerator</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/50434617-E70E-4931-B98E-61650E9DEA7E">IAudioFormatEnumerator</a> that contains  all supported audio formats for spatial audio objects, the first item in the list represents the most preferable format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47AB0B3B-E8D0-412F-AC9C-F8BC700E7C23">IsAudioObjectFormatSupported</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a> supports a the specified format. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4CE8A0D2-8B0B-4628-99DE-5B588842D7C5">IsSpatialAudioStreamAvailable</a>
</td>
<td align="left" width="63%">
When successful, gets a value indicating whether the currently active spatial rendering engine supports the specified spatial audio render stream. 

</td>
</tr>
</table> 


## -remarks



Get an instance of this interface by calling <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>, using the  <a href="https://msdn.microsoft.com/en-us/library/zaah6a61.aspx">__uuidof</a> operator to get the class ID of the <b>ISpatialAudioClient</b> interface. The following example code shows how to initialize this interface.


```cpp
PROPVARIANT var; 
PropVariantInit(&var);  
auto p = reinterpret_cast<SpatialAudioClientActivationParams *>(CoTaskMemAlloc(sizeof(SpatialAudioClientActivationParams)));  
if (nullptr == p) { ... } 
p->tracingContextId = /* context identifier */;  
p->appId = /* app identifier */;  
p->majorVersion = /* app version info */;  
p->majorVersionN = /* app version info */;
var.vt = VT_BLOB;
var.blob.cbSize = sizeof(*p);
var.blob.pBlobData = reinterpret_cast<BYTE *>(p); 
hr = ActivateAudioInterfaceAsync(device, __uuidof(ISpatialAudioClient), &var, ...);
// ...
ropVariantClear(&var);
```


<div class="alert"><b>Note</b>  When using the <b>ISpatialAudioClient</b> interfaces on an Xbox One Development Kit (XDK) title, you must first call <b>EnableSpatialAudio</b> before calling <a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a> or <a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>. Failure to do so will result in an E_NOINTERFACE error being returned from the call to Activate. <b>EnableSpatialAudio</b> is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</div>
<div> </div>
To access the <b>ActivateAudioIntefaceAsync</b>, you will need to link to mmdevapi.lib.



