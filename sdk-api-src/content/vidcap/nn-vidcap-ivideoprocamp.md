---
UID: NN:vidcap.IVideoProcAmp
title: IVideoProcAmp (vidcap.h)
author: windows-sdk-content
description: The IVideoProcAmp interface controls the image adjustment (ProcAmp) settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
old-location: dshow\ivideoprocamp.htm
tech.root: DirectShow
ms.assetid: efaef34a-688a-4c7d-b8ee-e0f52468e355
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp, IVideoProcAmp interface [DirectShow], IVideoProcAmp interface [DirectShow],described, IVideoProcAmpInterface, dshow.ivideoprocamp, vidcap/IVideoProcAmp
ms.topic: interface
f1_keywords: 
 - "vidcap/IVideoProcAmp"
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vidcap.h
api_name:
 - IVideoProcAmp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp interface


## -description



The <code>IVideoProcAmp</code> interface controls the image adjustment (ProcAmp) settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo</a> interface. For each node, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodetype">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>IVideoProcAmp</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_PROCESSING. Get the interface pointer by calling <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_IVideoProcAmp.

This interface corresponds to the PROPSETID_VIDCAP_VIDEOPROCAMP property set, which is documented in the Windows DDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoProcAmp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVideoProcAmp</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_backlightcompensation">get_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the camera's backlight compensation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_brightness">get_Brightness</a>
</td>
<td align="left" width="63%">
Returns the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_colorenable">get_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_contrast">get_Contrast</a>
</td>
<td align="left" width="63%">
Returns the camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_digitalmultiplier">get_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_gain">get_Gain</a>
</td>
<td align="left" width="63%">
Returns the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_gamma">get_Gamma</a>
</td>
<td align="left" width="63%">
Returns the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_hue">get_Hue</a>
</td>
<td align="left" width="63%">
Returns the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_powerlinefrequency">get_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_saturation">get_Saturation</a>
</td>
<td align="left" width="63%">
Returns the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_sharpness">get_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_whitebalance">get_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_whitebalancecomponent">get_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_backlightcompensation">getRange_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the range of backlight compensation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_brightness">getRange_Brightness</a>
</td>
<td align="left" width="63%">
Returns the range of brightness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_colorenable">getRange_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the range of color-enable settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_contrast">getRange_Contrast</a>
</td>
<td align="left" width="63%">
Returns the range of contrast settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_digitalmultiplier">getRange_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the range of digital zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_gain">getRange_Gain</a>
</td>
<td align="left" width="63%">
Returns the range of gain settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_gamma">getRange_Gamma</a>
</td>
<td align="left" width="63%">
Returns the range of gamma settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_hue">getRange_Hue</a>
</td>
<td align="left" width="63%">
Returns the range of hue settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_powerlinefrequency">getRange_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the range of power line frequency settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_saturation">getRange_Saturation</a>
</td>
<td align="left" width="63%">
Returns the range of saturation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_sharpness">getRange_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the range of sharpness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_whitebalance">getRange_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_whitebalancecomponent">getRange_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_backlightcompensation">put_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Sets the camera's backlight compensation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_brightness">put_Brightness</a>
</td>
<td align="left" width="63%">
Sets the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_colorenable">put_ColorEnable</a>
</td>
<td align="left" width="63%">
Sets the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_contrast">put_Contrast</a>
</td>
<td align="left" width="63%">
Sets camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_digitalmultiplier">put_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Sets the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_gain">put_Gain</a>
</td>
<td align="left" width="63%">
Sets the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_gamma">put_Gamma</a>
</td>
<td align="left" width="63%">
Sets the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_hue">put_Hue</a>
</td>
<td align="left" width="63%">
Sets the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_powerlinefrequency">put_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Sets the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_saturation">put_Saturation</a>
</td>
<td align="left" width="63%">
Sets the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_sharpness">put_Sharpness</a>
</td>
<td align="left" width="63%">
Sets the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_whitebalance">put_WhiteBalance</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-put_whitebalancecomponent">put_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as red and blue component values.

</td>
</tr>
</table> 

