---
UID: NN:vidcap.ICameraControl
title: ICameraControl (vidcap.h)
author: windows-sdk-content
description: The ICameraControl interface controls the camera settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
old-location: dshow\icameracontrol.htm
tech.root: DirectShow
ms.assetid: 7046f96d-a613-4056-84dd-be022efdda4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], ICameraControl interface [DirectShow],described, ICameraControlInterface, dshow.icameracontrol, vidcap/ICameraControl
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl interface


## -description



The <code>ICameraControl</code> interface controls the camera settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://msdn.microsoft.com/en-us/library/Dd390148(v=VS.85).aspx">IKsTopologyInfo</a> interface. For each node, call <a href="https://msdn.microsoft.com/en-us/library/Dd390153(v=VS.85).aspx">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>ICameraControl</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_CAMERA_TERMINAL. Get the interface pointer by calling <a href="https://msdn.microsoft.com/en-us/library/Dd390149(v=VS.85).aspx">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_ICameraControl.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd376313(v=VS.85).aspx">get_Exposure</a>
</td>
<td align="left" width="63%">
Returns the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376314(v=VS.85).aspx">get_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376315(v=VS.85).aspx">get_FocalLengths</a>
</td>
<td align="left" width="63%">
Returns the focal lengths of the camera lenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376316(v=VS.85).aspx">get_Focus</a>
</td>
<td align="left" width="63%">
Returns the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376317(v=VS.85).aspx">get_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376318(v=VS.85).aspx">get_Iris</a>
</td>
<td align="left" width="63%">
Returns the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376319(v=VS.85).aspx">get_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376320(v=VS.85).aspx">get_Pan</a>
</td>
<td align="left" width="63%">
Returns the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376321(v=VS.85).aspx">get_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376322(v=VS.85).aspx">get_PanTilt</a>
</td>
<td align="left" width="63%">
Returns the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376323(v=VS.85).aspx">get_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376324(v=VS.85).aspx">get_PrivacyMode</a>
</td>
<td align="left" width="63%">
Returns the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376325(v=VS.85).aspx">get_Roll</a>
</td>
<td align="left" width="63%">
Returns the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376326(v=VS.85).aspx">get_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376327(v=VS.85).aspx">get_ScanMode</a>
</td>
<td align="left" width="63%">
Returns the current scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376328(v=VS.85).aspx">get_Tilt</a>
</td>
<td align="left" width="63%">
Returns the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376329(v=VS.85).aspx">get_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376330(v=VS.85).aspx">get_Zoom</a>
</td>
<td align="left" width="63%">
Returns the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376331(v=VS.85).aspx">get_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative zoom.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376299(v=VS.85).aspx">getRange_Exposure</a>
</td>
<td align="left" width="63%">
Returns the range of exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376300(v=VS.85).aspx">getRange_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376301(v=VS.85).aspx">getRange_Focus</a>
</td>
<td align="left" width="63%">
Returns the range of focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376302(v=VS.85).aspx">getRange_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376303(v=VS.85).aspx">getRange_Iris</a>
</td>
<td align="left" width="63%">
Returns the range of aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376304(v=VS.85).aspx">getRange_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376305(v=VS.85).aspx">getRange_Pan</a>
</td>
<td align="left" width="63%">
Returns the range of panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376306(v=VS.85).aspx">getRange_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376307(v=VS.85).aspx">getRange_Roll</a>
</td>
<td align="left" width="63%">
Returns the range of roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376308(v=VS.85).aspx">getRange_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376309(v=VS.85).aspx">getRange_Tilt</a>
</td>
<td align="left" width="63%">
Returns the range of tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376310(v=VS.85).aspx">getRange_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376311(v=VS.85).aspx">getRange_Zoom</a>
</td>
<td align="left" width="63%">
Returns the range of zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376312(v=VS.85).aspx">getRange_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376332(v=VS.85).aspx">put_Exposure</a>
</td>
<td align="left" width="63%">
Sets the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376334(v=VS.85).aspx">put_ExposureRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376335(v=VS.85).aspx">put_Focus</a>
</td>
<td align="left" width="63%">
Sets the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376336(v=VS.85).aspx">put_FocusRelative</a>
</td>
<td align="left" width="63%">
Sets the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376337(v=VS.85).aspx">put_Iris</a>
</td>
<td align="left" width="63%">
Sets the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376338(v=VS.85).aspx">put_IrisRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376339(v=VS.85).aspx">put_Pan</a>
</td>
<td align="left" width="63%">
Sets the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376340(v=VS.85).aspx">put_PanRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376341(v=VS.85).aspx">put_PanTilt</a>
</td>
<td align="left" width="63%">
Sets the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376342(v=VS.85).aspx">put_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376343(v=VS.85).aspx">put_PrivacyMode</a>
</td>
<td align="left" width="63%">
Sets the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376344(v=VS.85).aspx">put_Roll</a>
</td>
<td align="left" width="63%">
Sets the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376345(v=VS.85).aspx">put_RollRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376346(v=VS.85).aspx">put_ScanMode</a>
</td>
<td align="left" width="63%">
Sets the camera's scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376347(v=VS.85).aspx">put_Tilt</a>
</td>
<td align="left" width="63%">
Sets the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376348(v=VS.85).aspx">put_TiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376349(v=VS.85).aspx">put_Zoom</a>
</td>
<td align="left" width="63%">
Sets the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376350(v=VS.85).aspx">put_ZoomRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative zoom.

</td>
</tr>
</table> 

