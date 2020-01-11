---
UID: NN:vidcap.ICameraControl
title: ICameraControl (vidcap.h)
description: The ICameraControl interface controls the camera settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
old-location: dshow\icameracontrol.htm
tech.root: DirectShow
ms.assetid: 7046f96d-a613-4056-84dd-be022efdda4f
ms.date: 12/05/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], ICameraControl interface [DirectShow],described, ICameraControlInterface, dshow.icameracontrol, vidcap/ICameraControl
f1_keywords:
- vidcap/ICameraControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl interface


## -description



The <code>ICameraControl</code> interface controls the camera settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo</a> interface. For each node, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodetype">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>ICameraControl</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_CAMERA_TERMINAL. Get the interface pointer by calling <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_ICameraControl.

This interface corresponds to the PROPSETID_VIDCAP_CAMERACONTROL property set, which is documented in the Windows DDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICameraControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_exposure">get_Exposure</a>
</td>
<td align="left" width="63%">
Returns the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_exposurerelative">get_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focallengths">get_FocalLengths</a>
</td>
<td align="left" width="63%">
Returns the focal lengths of the camera lenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focus">get_Focus</a>
</td>
<td align="left" width="63%">
Returns the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focusrelative">get_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_iris">get_Iris</a>
</td>
<td align="left" width="63%">
Returns the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_irisrelative">get_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_pan">get_Pan</a>
</td>
<td align="left" width="63%">
Returns the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_panrelative">get_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_pantilt">get_PanTilt</a>
</td>
<td align="left" width="63%">
Returns the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_pantiltrelative">get_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_privacymode">get_PrivacyMode</a>
</td>
<td align="left" width="63%">
Returns the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_roll">get_Roll</a>
</td>
<td align="left" width="63%">
Returns the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_rollrelative">get_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_scanmode">get_ScanMode</a>
</td>
<td align="left" width="63%">
Returns the current scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_tilt">get_Tilt</a>
</td>
<td align="left" width="63%">
Returns the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_tiltrelative">get_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_zoom">get_Zoom</a>
</td>
<td align="left" width="63%">
Returns the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_zoomrelative">get_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the camera's relative zoom.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_exposure">getRange_Exposure</a>
</td>
<td align="left" width="63%">
Returns the range of exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_exposurerelative">getRange_ExposureRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative exposure times supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_focus">getRange_Focus</a>
</td>
<td align="left" width="63%">
Returns the range of focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_focusrelative">getRange_FocusRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative focal distances supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_iris">getRange_Iris</a>
</td>
<td align="left" width="63%">
Returns the range of aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_irisrelative">getRange_IrisRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative aperture settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_pan">getRange_Pan</a>
</td>
<td align="left" width="63%">
Returns the range of panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_panrelative">getRange_PanRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative panning angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_roll">getRange_Roll</a>
</td>
<td align="left" width="63%">
Returns the range of roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_rollrelative">getRange_RollRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative roll angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tilt">getRange_Tilt</a>
</td>
<td align="left" width="63%">
Returns the range of tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tiltrelative">getRange_TiltRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative tilt angles supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_zoom">getRange_Zoom</a>
</td>
<td align="left" width="63%">
Returns the range of zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_zoomrelative">getRange_ZoomRelative</a>
</td>
<td align="left" width="63%">
Returns the range of relative zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_exposure">put_Exposure</a>
</td>
<td align="left" width="63%">
Sets the camera's exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_exposurerelative">put_ExposureRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative exposure time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_focus">put_Focus</a>
</td>
<td align="left" width="63%">
Sets the distance that is optimally in focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_focusrelative">put_FocusRelative</a>
</td>
<td align="left" width="63%">
Sets the relative focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_iris">put_Iris</a>
</td>
<td align="left" width="63%">
Sets the camera's aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_irisrelative">put_IrisRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative aperture setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_pan">put_Pan</a>
</td>
<td align="left" width="63%">
Sets the camera's panning angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_panrelative">put_PanRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_pantilt">put_PanTilt</a>
</td>
<td align="left" width="63%">
Sets the camera's pan and tilt angles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_pantiltrelative">put_PanTiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative pan and tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_privacymode">put_PrivacyMode</a>
</td>
<td align="left" width="63%">
Sets the camera's privacy setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_roll">put_Roll</a>
</td>
<td align="left" width="63%">
Sets the camera's roll angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_rollrelative">put_RollRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative roll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_scanmode">put_ScanMode</a>
</td>
<td align="left" width="63%">
Sets the camera's scanning mode (interlaced or progressive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_tilt">put_Tilt</a>
</td>
<td align="left" width="63%">
Sets the camera's tilt angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_tiltrelative">put_TiltRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative tilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_zoom">put_Zoom</a>
</td>
<td align="left" width="63%">
Sets the camera's zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_zoomrelative">put_ZoomRelative</a>
</td>
<td align="left" width="63%">
Sets the camera's relative zoom.

</td>
</tr>
</table> 

