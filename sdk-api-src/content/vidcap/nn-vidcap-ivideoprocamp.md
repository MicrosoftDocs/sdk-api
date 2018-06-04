---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IVideoProcAmp interface


## -description



The <code>IVideoProcAmp</code> interface controls the image adjustment (ProcAmp) settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo</a> interface. For each node, call <a href="https://msdn.microsoft.com/6606d563-6a35-4595-8bb2-6cf74f7af4e7">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>IVideoProcAmp</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_PROCESSING. Get the interface pointer by calling <a href="https://msdn.microsoft.com/f2c7ea1d-abd6-4179-b5b7-d89837ceecd7">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_IVideoProcAmp.

This interface corresponds to the PROPSETID_VIDCAP_VIDEOPROCAMP property set, which is documented in the Windows DDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoProcAmp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVideoProcAmp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVideoProcAmp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b0b4c06-5958-446e-bd06-4ee6f90b6e78">get_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the camera's backlight compensation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0e3b7cf-c133-4b47-8209-1014d1e3d671">get_Brightness</a>
</td>
<td align="left" width="63%">
Returns the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6097b8cf-b46e-443d-8f32-46eb4a8f4de6">get_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c63013-33f1-42c0-9239-ec012c9a0528">get_Contrast</a>
</td>
<td align="left" width="63%">
Returns the camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b7ab1a3-193c-4682-af35-ae0cc5f28f45">get_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36d84db9-4a53-4087-b389-e707ed3d5572">get_Gain</a>
</td>
<td align="left" width="63%">
Returns the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8d62862-5509-4401-affe-68dfa96ae60f">get_Gamma</a>
</td>
<td align="left" width="63%">
Returns the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfdd44b5-fd39-40da-95b8-9008aef10f9a">get_Hue</a>
</td>
<td align="left" width="63%">
Returns the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c7bfc4a-895f-45a6-9619-868d1e7bc674">get_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977e71a4-8118-4fc2-9f76-ec30293b33d0">get_Saturation</a>
</td>
<td align="left" width="63%">
Returns the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12cb9934-4cef-4356-9b59-6b4e6caca573">get_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53743bff-4257-4abf-b41a-aa5586ab37b5">get_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9beb89f-df55-4b76-a679-5e27cb0af9fb">get_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4527e7e9-372c-4883-a068-1ce53eb2256a">getRange_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the range of backlight compensation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/236f919a-5ed3-4ce4-877e-023af1a4e4d0">getRange_Brightness</a>
</td>
<td align="left" width="63%">
Returns the range of brightness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9041f2a-cf38-419b-be8f-a55599b9a1d9">getRange_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the range of color-enable settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eb160f4-c3e6-4c74-a091-72c55416a81e">getRange_Contrast</a>
</td>
<td align="left" width="63%">
Returns the range of contrast settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a8a5f72-d51f-4f5a-95e4-ac8d1ac1b24f">getRange_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the range of digital zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a039cece-ee44-43e0-ade9-5a7e1d9a1c11">getRange_Gain</a>
</td>
<td align="left" width="63%">
Returns the range of gain settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36914aed-d11c-42c0-a0e5-ba1d3ba6dd22">getRange_Gamma</a>
</td>
<td align="left" width="63%">
Returns the range of gamma settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5625b73c-8033-4930-af26-e7c4b4fb6516">getRange_Hue</a>
</td>
<td align="left" width="63%">
Returns the range of hue settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6bb1df3-d033-4627-b5ea-574a2ebf43aa">getRange_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the range of power line frequency settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c3d99a4-fc23-4d5e-907e-72272599a684">getRange_Saturation</a>
</td>
<td align="left" width="63%">
Returns the range of saturation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a5fe298-e76b-44ac-9fcd-a5d1aeb3593c">getRange_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the range of sharpness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c7a21ec-2aa5-4e00-8d7b-a13a366a3f17">getRange_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dec23c5a-3999-4f9b-81f3-2718b38d5835">getRange_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52a9a841-b3d0-41fe-b531-70fa6bac4517">put_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Sets the camera's backlight compensation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69c8086c-a638-4ec6-a4fd-5a400095145d">put_Brightness</a>
</td>
<td align="left" width="63%">
Sets the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a1caa3f-e591-4176-90b9-80a4bd71533b">put_ColorEnable</a>
</td>
<td align="left" width="63%">
Sets the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a03ab735-2258-49c6-a66a-fabe38f88532">put_Contrast</a>
</td>
<td align="left" width="63%">
Sets camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1832aad-22fc-41f0-a99a-09b56c148384">put_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Sets the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8256c1d9-ca3f-4b6a-921d-a424932927b5">put_Gain</a>
</td>
<td align="left" width="63%">
Sets the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4efe538-75c5-4c52-9ad2-dc6badee74f2">put_Gamma</a>
</td>
<td align="left" width="63%">
Sets the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b0926c3-4167-423d-ac5c-ac4df06948aa">put_Hue</a>
</td>
<td align="left" width="63%">
Sets the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef490cec-4f25-432a-b6a5-3e16044314e4">put_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Sets the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7167fcac-b0c8-444e-a6a9-7ff9a603cc58">put_Saturation</a>
</td>
<td align="left" width="63%">
Sets the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a47e8f21-29ec-4845-97b2-1a9d6478afa6">put_Sharpness</a>
</td>
<td align="left" width="63%">
Sets the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b79e64e1-4b0f-4111-ae25-54891f743c01">put_WhiteBalance</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/800d7ddb-9f66-4fc4-a246-e6501377b9ce">put_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as red and blue component values.

</td>
</tr>
</table> 

