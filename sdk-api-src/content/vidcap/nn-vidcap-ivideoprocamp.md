---
UID: NN:vidcap.IVideoProcAmp
title: IVideoProcAmp
author: windows-sdk-content
description: The IVideoProcAmp interface controls the image adjustment (ProcAmp) settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
old-location: dshow\ivideoprocamp.htm
tech.root: DirectShow
ms.assetid: efaef34a-688a-4c7d-b8ee-e0f52468e355
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp, IVideoProcAmp interface [DirectShow], IVideoProcAmp interface [DirectShow],described, IVideoProcAmpInterface, dshow.ivideoprocamp, vidcap/IVideoProcAmp
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp interface


## -description



The <code>IVideoProcAmp</code> interface controls the image adjustment (ProcAmp) settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="https://msdn.microsoft.com/en-us/library/Dd390148(v=VS.85).aspx">IKsTopologyInfo</a> interface. For each node, call <a href="https://msdn.microsoft.com/en-us/library/Dd390153(v=VS.85).aspx">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>IVideoProcAmp</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_PROCESSING. Get the interface pointer by calling <a href="https://msdn.microsoft.com/en-us/library/Dd390149(v=VS.85).aspx">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_IVideoProcAmp.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd377250(v=VS.85).aspx">get_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the camera's backlight compensation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377251(v=VS.85).aspx">get_Brightness</a>
</td>
<td align="left" width="63%">
Returns the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377252(v=VS.85).aspx">get_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377253(v=VS.85).aspx">get_Contrast</a>
</td>
<td align="left" width="63%">
Returns the camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377254(v=VS.85).aspx">get_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377255(v=VS.85).aspx">get_Gain</a>
</td>
<td align="left" width="63%">
Returns the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377256(v=VS.85).aspx">get_Gamma</a>
</td>
<td align="left" width="63%">
Returns the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377257(v=VS.85).aspx">get_Hue</a>
</td>
<td align="left" width="63%">
Returns the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377258(v=VS.85).aspx">get_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377259(v=VS.85).aspx">get_Saturation</a>
</td>
<td align="left" width="63%">
Returns the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377260(v=VS.85).aspx">get_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377261(v=VS.85).aspx">get_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377262(v=VS.85).aspx">get_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the camera's white balance, specified as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377237(v=VS.85).aspx">getRange_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Returns the range of backlight compensation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377238(v=VS.85).aspx">getRange_Brightness</a>
</td>
<td align="left" width="63%">
Returns the range of brightness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377239(v=VS.85).aspx">getRange_ColorEnable</a>
</td>
<td align="left" width="63%">
Returns the range of color-enable settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377240(v=VS.85).aspx">getRange_Contrast</a>
</td>
<td align="left" width="63%">
Returns the range of contrast settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377241(v=VS.85).aspx">getRange_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Returns the range of digital zoom levels supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377242(v=VS.85).aspx">getRange_Gain</a>
</td>
<td align="left" width="63%">
Returns the range of gain settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377243(v=VS.85).aspx">getRange_Gamma</a>
</td>
<td align="left" width="63%">
Returns the range of gamma settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377244(v=VS.85).aspx">getRange_Hue</a>
</td>
<td align="left" width="63%">
Returns the range of hue settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377245(v=VS.85).aspx">getRange_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Returns the range of power line frequency settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377246(v=VS.85).aspx">getRange_Saturation</a>
</td>
<td align="left" width="63%">
Returns the range of saturation settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377247(v=VS.85).aspx">getRange_Sharpness</a>
</td>
<td align="left" width="63%">
Returns the range of sharpness settings supported by the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377248(v=VS.85).aspx">getRange_WhiteBalance</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377249(v=VS.85).aspx">getRange_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Returns the range of white balance settings supported by the camera, expressed as red and blue component values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377263(v=VS.85).aspx">put_BacklightCompensation</a>
</td>
<td align="left" width="63%">
Sets the camera's backlight compensation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377264(v=VS.85).aspx">put_Brightness</a>
</td>
<td align="left" width="63%">
Sets the camera's brightness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377265(v=VS.85).aspx">put_ColorEnable</a>
</td>
<td align="left" width="63%">
Sets the camera's color-enable setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377266(v=VS.85).aspx">put_Contrast</a>
</td>
<td align="left" width="63%">
Sets camera's contrast setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377267(v=VS.85).aspx">put_DigitalMultiplier</a>
</td>
<td align="left" width="63%">
Sets the camera's digital zoom level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377268(v=VS.85).aspx">put_Gain</a>
</td>
<td align="left" width="63%">
Sets the camera's gain setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377269(v=VS.85).aspx">put_Gamma</a>
</td>
<td align="left" width="63%">
Sets the camera's gamma setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377270(v=VS.85).aspx">put_Hue</a>
</td>
<td align="left" width="63%">
Sets the camera's hue setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377271(v=VS.85).aspx">put_PowerlineFrequency</a>
</td>
<td align="left" width="63%">
Sets the camera's power line frequency setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377272(v=VS.85).aspx">put_Saturation</a>
</td>
<td align="left" width="63%">
Sets the camera's saturation setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377273(v=VS.85).aspx">put_Sharpness</a>
</td>
<td align="left" width="63%">
Sets the camera's sharpness setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377274(v=VS.85).aspx">put_WhiteBalance</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as a color temperature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377275(v=VS.85).aspx">put_WhiteBalanceComponent</a>
</td>
<td align="left" width="63%">
Sets the camera's white balance, specified as red and blue component values.

</td>
</tr>
</table> 

