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



The <b>IMSVidCtl</b> interface is the main interface for the <a href="https://msdn.microsoft.com/743a1950-4f70-45a1-9536-0d75064f401b">Video Control</a>. It contains methods to enumerate available devices and features, and to select which features and devices will be active. It also contains methods to build, stop, start, and pause the filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidCtl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMSVidCtl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">Build</a>
</td>
<td align="left" width="63%">
Builds the underlying filter graph and connects all the filters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e67bf380-dc2c-42c9-a995-17951c65fbda">Decompose</a>
</td>
<td align="left" width="63%">
Disassembles the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0166cdc3-de1c-4505-855e-f69144cc71aa">DisableAudio</a>
</td>
<td align="left" width="63%">
Disables the audio output device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c8f7af1-0416-4860-aa05-d2167452291e">DisableVideo</a>
</td>
<td align="left" width="63%">
Disables the video output device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d77eca3-aec9-423d-8d02-92e6f9ab5167">get__InputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of inputs available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8242712a-9112-456b-b76d-1f382c9b637f">get__OutputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of outputs for a specified category that are available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">get_AudioRendererActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active audio renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ab81536-2701-408e-be3a-f44375ef8193">get_AudioRenderersAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection containing the available audio renderers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8adbc701-fd05-4520-8f06-95bd67a08d1e">get_AutoSize</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f67f1f9-e4e1-47fc-a92d-b6dfb65e7ec9">get_BackColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f197faf-a91e-4984-8858-ceab6506b273">get_ColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3d5ed73-4781-46fb-8df4-a7dc339b755c">get_DisplaySize</a>
</td>
<td align="left" width="63%">
Retrieves the display size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c1ec2a6-9880-4420-8d28-4374f1658bd9">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the Video Control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33832fe2-e8ef-4e37-9af9-90f566feb559">get_FeaturesActive</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the features that are currently active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73da686c-0c25-4dfb-8a13-681f1dac6a4a">get_FeaturesAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of features available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3451002b-5339-4b43-aefd-d66c48f7ae57">get_InputActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active input device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ed22c3e-745a-4680-a5fc-accef56ab348">get_InputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of inputs available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eebb75d2-d5ee-49d6-b1bf-03b0040564b7">get_MaintainAspectRatio</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Video Control should maintain the aspect ratio of the source video when resizing its own rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9465ff38-c524-47e1-8bc0-bd6b2e0dea8c">get_OutputsActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active output device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f45b752c-6b7f-4803-93fe-92ec44cd9509">get_OutputsAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of outputs for a specified category that are available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45f35832-709c-4f78-9e1a-a6ad489fc81f">get_State</a>
</td>
<td align="left" width="63%">
Retrieves the state of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9579144d-22b6-4d97-a52c-0d8bbc9066e4">get_TabStop</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a user can use the TAB key to give the focus to the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b69abaf-95ab-49b9-9555-a2244224cb5d">get_VideoRendererActive</a>
</td>
<td align="left" width="63%">
Retrieves the currently active video renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20e5b2f3-33ea-4b0d-84b8-e4b0b61e0348">get_VideoRenderersAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a collection of video renderers available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88121bed-c626-4c1a-b415-8d162c43df9d">get_Window</a>
</td>
<td align="left" width="63%">
Retrieves the window handle associated with the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd7687d8-325f-4a51-ab57-ffcc45a9157b">Pause</a>
</td>
<td align="left" width="63%">
Pauses the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f6498ce-fb53-4d57-b6bd-6696ba57de3b">put_AudioRendererActive</a>
</td>
<td align="left" width="63%">
Sets the currently active audio renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb5863e2-380b-4bee-ac18-e5f28551a6ab">put_AutoSize</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the Video Control is automatically resized to display its entire contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2812c19-2b69-46a8-98ab-7e1eee43f383">put_BackColor</a>
</td>
<td align="left" width="63%">
Sets the background color of the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2896f062-4ff9-4652-89b9-5fe55c6fe472">put_ColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1771e66b-e5f3-44f5-a489-e57baaf5cf25">put_DisplaySize</a>
</td>
<td align="left" width="63%">
Sets the display size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/366164ac-1514-46d6-870a-388706b8de75">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the Video Control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293506fa-3208-468e-982a-3c1f8ce0269b">put_FeaturesActive</a>
</td>
<td align="left" width="63%">
Sets a collection of the features that are currently active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">put_InputActive</a>
</td>
<td align="left" width="63%">
Sets the currently active input device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f0943b1-3cb9-46dc-8aaf-be22e2464092">put_MaintainAspectRatio</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the Video Control should maintain the aspect ratio of the source video when resizing its own rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/636cedef-f6e5-40f2-8f1c-9f886d618ad0">put_OutputsActive</a>
</td>
<td align="left" width="63%">
Sets the currently active output device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0e3d216-ea3f-4db4-80fd-aaf4d520ba1a">put_TabStop</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether a user can use the TAB key to give the focus to the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb6e1db7-b980-4706-a1f1-cd6d8423bfb2">put_VideoRendererActive</a>
</td>
<td align="left" width="63%">
Sets the currently active video renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7413049e-3ce4-46e9-ab49-fbdb0455c6b6">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the graph configuration and the video display rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37ed6d7b-2e44-4bce-b476-8e8b28635346">Run</a>
</td>
<td align="left" width="63%">
Runs the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ca43663-3726-4147-8774-2f1eecef9142">Stop</a>
</td>
<td align="left" width="63%">
Stops the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">View</a>
</td>
<td align="left" width="63%">
Selects an input device that is capable of handling a specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23b83339-f712-4b49-91f9-d0a1b02d64af">ViewNext</a>
</td>
<td align="left" width="63%">
Finds another input device for viewing the specified item.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidCtl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/ff269a7a-3b9e-4125-8be1-594327e7177c">Using the Video Control</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

