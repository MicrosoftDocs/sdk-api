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

# IWMReaderAdvanced interface


## -description



A call to <b>QueryInterface</b> from a reader object exposes the advanced functionality described in this section.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e47ef96-9971-47b0-a003-b38f4045da7a">DeliverTime</a>
</td>
<td align="left" width="63%">
Provides the reader with a clock time. This is used only when the application is providing the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0da74ff-37d9-4bb3-85f2-f8e1585c2d7f">GetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/816f13b1-9856-482d-b5b1-4aaf5c61c230">GetAllocateForStream</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3205f508-a24b-4d24-a5e6-be16885e941b">GetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Ascertains whether manual stream selection has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad21ab6e-c7af-4293-8920-05db62b9f7ef">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for output samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9511c269-0f88-4fdd-8d4b-c52bace14791">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7923564d-23d5-4163-9316-347c466c7dc0">GetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Retrieves a flag that indicates whether receiving stream selection notifications has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdb76a25-fc30-4be2-a54e-928050699e58">GetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to deliver stream samples (compressed samples).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ed2a3fe-c31d-42fc-9ee9-27dd9aef7e06">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves the current reader statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/083fc743-79be-43c6-ac4b-458c74f42fa0">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Ascertains whether a particular stream is currently selected. This can be used only when manual stream selection is specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54eb30ae-4b84-489c-a5e5-e73dee2c5056">GetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Ascertains whether a user-provided clock has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d2470c-e6ce-4f3f-b4f8-0bc65a2a8bfd">NotifyLateDelivery</a>
</td>
<td align="left" width="63%">
Used to notify the reader that it is delivering data to the application too slowly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fba76c75-6179-4e10-9a3c-8e604e392cca">SetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58c396a9-5d1e-4a13-a877-5289649a6375">SetAllocateForStream</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dec93690-8285-4672-bf70-63f3c10294bf">SetClientInfo</a>
</td>
<td align="left" width="63%">
Sets client-side information used for logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6950b26c-1763-4578-ab5c-0ea29d3d77f1">SetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Specifies whether stream selection is to be controlled manually.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cb0bd59-2a46-4cdc-9a88-ee6a8f170f3c">SetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Specifies a flag indicating whether receiving selection callbacks is to be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fb39726-7f43-41ec-9ead-38456b5cd964">SetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Specifies whether the reader must deliver compressed stream samples to the callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/921ab9fe-757f-4856-9fbc-b615bf92d90f">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Enables the selected state of a stream to be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f29beea-1da4-41e0-a68d-93af3b1f55ed">SetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Specifies that a clock provided by the application is to be used.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/28d697d8-99b5-4968-a765-ba01b86914f6">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/95e8c151-9aae-4930-824c-8809dfc07705">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

