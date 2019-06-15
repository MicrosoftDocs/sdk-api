---
UID: NN:msvidctl.IMSVidCtl
title: IMSVidCtl (msvidctl.h)
author: windows-sdk-content
description: The IMSVidCtl interface is the main interface for the Video Control.
old-location: mstv\imsvidctl.htm
tech.root: mstv
ms.assetid: e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], IMSVidCtl interface [Microsoft TV Technologies],described, IMSVidCtlInterface, mstv.imsvidctl, msvidctl/IMSVidCtl
ms.topic: interface
f1_keywords: ["msvidctl/IMSVidCtl"]
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - msvidctl.h
api_name:
 - IMSVidCtl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl interface


## -description



The <b>IMSVidCtl</b> interface is the main interface for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ee663618(v=vs.85)">Video Control</a>. It contains methods to enumerate available devices and features, and to select which features and devices will be active. It also contains methods to build, stop, start, and pause the filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidCtl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidCtl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidCtl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">Build</a>
</td>
<td align="left" width="63%">
Builds the underlying filter graph and connects all the filters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-decompose">Decompose</a>
</td>
<td align="left" width="63%">
Disassembles the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-disableaudio">DisableAudio</a>
</td>
<td align="left" width="63%">
Disables the audio output device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-disablevideo">DisableVideo</a>
</td>
<td align="left" width="63%">
Disables the video output device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get__inputsavailable">get__InputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of inputs available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get__outputsavailable">get__OutputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of outputs for a specified category that are available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">get_AudioRendererActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active audio renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorenderersavailable">get_AudioRenderersAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection containing the available audio renderers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_autosize">get_AutoSize</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_backcolor">get_BackColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_colorkey">get_ColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_displaysize">get_DisplaySize</a>
</td>
<td align="left" width="63%">
Retrieves the display size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the Video Control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_featuresactive">get_FeaturesActive</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the features that are currently active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_featuresavailable">get_FeaturesAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of features available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputactive">get_InputActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active input device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputsavailable">get_InputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of inputs available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_maintainaspectratio">get_MaintainAspectRatio</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Video Control should maintain the aspect ratio of the source video when resizing its own rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_outputsactive">get_OutputsActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active output device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_outputsavailable">get_OutputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of outputs for a specified category that are available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_state">get_State</a>
</td>
<td align="left" width="63%">
Retrieves the state of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_tabstop">get_TabStop</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a user can use the TAB key to give the focus to the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorendereractive">get_VideoRendererActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active video renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorenderersavailable">get_VideoRenderersAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of video renderers available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_window">get_Window</a>
</td>
<td align="left" width="63%">
Retrieves the window handle associated with the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_audiorendereractive">put_AudioRendererActive</a>
</td>
<td align="left" width="63%">
Sets the currently active audio renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_autosize">put_AutoSize</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the Video Control is automatically resized to display its entire contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_backcolor">put_BackColor</a>
</td>
<td align="left" width="63%">
Sets the background color of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_colorkey">put_ColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_displaysize">put_DisplaySize</a>
</td>
<td align="left" width="63%">
Sets the display size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_enabled">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the Video Control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_featuresactive">put_FeaturesActive</a>
</td>
<td align="left" width="63%">
Sets a collection of the features that are currently active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_inputactive">put_InputActive</a>
</td>
<td align="left" width="63%">
Sets the currently active input device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_maintainaspectratio">put_MaintainAspectRatio</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the Video Control should maintain the aspect ratio of the source video when resizing its own rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_outputsactive">put_OutputsActive</a>
</td>
<td align="left" width="63%">
Sets the currently active output device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_tabstop">put_TabStop</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether a user can use the TAB key to give the focus to the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_videorendereractive">put_VideoRendererActive</a>
</td>
<td align="left" width="63%">
Sets the currently active video renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the graph configuration and the video display rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-run">Run</a>
</td>
<td align="left" width="63%">
Runs the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">View</a>
</td>
<td align="left" width="63%">
Selects an input device that is capable of handling a specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-viewnext">ViewNext</a>
</td>
<td align="left" width="63%">
Finds another input device for viewing the specified item.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidCtl)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/using-the-video-control">Using the Video Control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

