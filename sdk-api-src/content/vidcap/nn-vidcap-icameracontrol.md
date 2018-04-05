---
UID: NN:vidcap.ICameraControl
title: ICameraControl
author: windows-driver-content
description: The ICameraControl interface controls the camera settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
old-location: dshow\icameracontrol.htm
old-project: DirectShow
ms.assetid: 7046f96d-a613-4056-84dd-be022efdda4f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], ICameraControl interface [DirectShow], described, ICameraControlInterface, dshow.icameracontrol, vidcap/ICameraControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIDEOHDR, *PVIDEOHDR, *LPVIDEOHDR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICameraControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl interface


## -description



The <code>ICameraControl</code> interface controls the camera settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo</a> interface. For each node, call <a href="https://msdn.microsoft.com/6606d563-6a35-4595-8bb2-6cf74f7af4e7">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>ICameraControl</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_CAMERA_TERMINAL. Get the interface pointer by calling <a href="https://msdn.microsoft.com/f2c7ea1d-abd6-4179-b5b7-d89837ceecd7">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_ICameraControl.

This interface corresponds to the PROPSETID_VIDCAP_CAMERACONTROL property set, which is documented in the Windows DDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICameraControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICameraControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19323477-8dc7-46ed-b6a3-d0dd8b103924">get_Exposure</a>
</td>
<td align="left" width="63%">
Returns the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d63cf869-ccb6-45cb-85ba-a1e41faa8086">get_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de566705-1f4b-4ffa-932d-a52521e6963b">get_FocalLengths</a>
</td>
<td align="left" width="63%">
Returns the focal lengths of the camera lenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59ab6306-539f-4be4-8e69-348eab6220ea">get_Focus</a>
</td>
<td align="left" width="63%">
Returns the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21bc1cbe-747b-4846-814f-1aed0ac614d6">get_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/710a29f1-f5ab-42cf-b912-dd9b4546757e">get_Iris</a>
</td>
<td align="left" width="63%">
Returns the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f01c00-ff18-4d58-a03b-9293a8a6a68c">get_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cbf7582-63ad-4572-be62-be1fe5bc60b3">get_Pan</a>
</td>
<td align="left" width="63%">
Returns the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7237e0a-82b3-4e2a-a6c7-97fbb03b5917">get_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88f67970-2946-49f9-9c90-e562f37edd83">get_PanTilt</a>
</td>
<td align="left" width="63%">
Returns the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d96dcfb-c0c4-4521-bf1f-30947577d305">get_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22bec1da-65ca-4101-8f30-8fbb537e5678">get_PrivacyMode</a>
</td>
<td align="left" width="63%">
Returns the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cebe99e1-9bcc-4826-8b15-b4d6757ec5b4">get_Roll</a>
</td>
<td align="left" width="63%">
Returns the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28fa7e55-8e43-40fc-ac6c-e19f91621405">get_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09a75986-9c5d-44fc-af62-297481854574">get_ScanMode</a>
</td>
<td align="left" width="63%">
Returns the current scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e9d9176-fb27-4221-876b-49f407289877">get_Tilt</a>
</td>
<td align="left" width="63%">
Returns the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8730043-a506-4c74-a9ca-94d6e003a4b1">get_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c1fe500-bccf-46ed-bcd9-f65b25e8ccb7">get_Zoom</a>
</td>
<td align="left" width="63%">
Returns the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1926541-d7c7-4a16-bbe7-0d93dec89c67">get_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative zoom.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e74ae3-6a07-47c8-8e6a-daf2cb32328c">getRange_Exposure</a>
</td>
<td align="left" width="63%">
Returns the range of exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab46e893-037a-42bb-a3ae-bef943cd6a5e">getRange_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2da5473-82c3-4719-bba6-04a1793a98eb">getRange_Focus</a>
</td>
<td align="left" width="63%">
Returns the range of focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5038a59-bdc4-4034-afd1-256003687187">getRange_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3bc5b0-18eb-470c-9922-1d401f43e269">getRange_Iris</a>
</td>
<td align="left" width="63%">
Returns the range of aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9816e29b-3366-49e7-aa4c-46b06963c176">getRange_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/390c6330-1eb4-4149-aabc-296b585b577a">getRange_Pan</a>
</td>
<td align="left" width="63%">
Returns the range of panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31affca6-e9e9-4715-aea4-0a39ce100556">getRange_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14400765-d8a2-4ac2-a26b-39949ecd2bda">getRange_Roll</a>
</td>
<td align="left" width="63%">
Returns the range of roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0208111-8648-4511-99f6-20489a026c91">getRange_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d48920cf-677e-4014-a998-426bb45d1b46">getRange_Tilt</a>
</td>
<td align="left" width="63%">
Returns the range of tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b78e961-8b05-4339-ad66-49f2d892d4dc">getRange_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a81b65-4b63-45c9-b065-f4aa5cf2e4ae">getRange_Zoom</a>
</td>
<td align="left" width="63%">
Returns the range of zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea3460b8-b956-4dc9-bed7-f28714e1df11">getRange_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db9bdb3-c508-40b6-bd5e-75e418ba2f18">put_Exposure</a>
</td>
<td align="left" width="63%">
Sets the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4afc3f7f-bba2-4160-b917-c792467d6305">put_ExposureRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c896bf2b-33b6-4e7c-bf84-b7dd8f57a4d4">put_Focus</a>
</td>
<td align="left" width="63%">
Sets the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d40edc5d-8fa2-4e3a-8aab-c51da0ac8036">put_FocusRelative</a>
</td>
<td align="left" width="63%">
Sets the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b181f556-3d3d-4622-8cc9-57fda50bf9c0">put_Iris</a>
</td>
<td align="left" width="63%">
Sets the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76cd3b1d-a6ce-4981-b82f-7ee83e118c33">put_IrisRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71dc3fe3-089c-46e8-a63b-7a638068d069">put_Pan</a>
</td>
<td align="left" width="63%">
Sets the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4ac28f4-8570-4307-80c1-2960d7c87544">put_PanRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9aa052a-72f9-4a17-bebe-809f43264481">put_PanTilt</a>
</td>
<td align="left" width="63%">
Sets the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69d8303c-2ff2-416d-909c-e9f352e53cf1">put_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04116eba-926c-43fc-9a45-91be42e9af26">put_PrivacyMode</a>
</td>
<td align="left" width="63%">
Sets the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f74c7acc-e141-4238-bcbe-7890646e706c">put_Roll</a>
</td>
<td align="left" width="63%">
Sets the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0dbfd1c-493f-4f35-88ab-cd3868a56370">put_RollRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d5d2bd-4aa4-49f6-a02f-c53af1333a1b">put_ScanMode</a>
</td>
<td align="left" width="63%">
Sets the camera's scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e75adedb-5cf2-4b2c-bb57-1bfedfc81979">put_Tilt</a>
</td>
<td align="left" width="63%">
Sets the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69aa7ecf-4816-460b-b4f8-480c0d4f8331">put_TiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6bb0206-04c4-4d93-b267-2881e58c0a14">put_Zoom</a>
</td>
<td align="left" width="63%">
Sets the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/815f92c3-bfab-47d5-86dd-f9b2321d20eb">put_ZoomRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative zoom.

</td>
</tr>
</table> 

