---
UID: NN:wmsdkidl.IWMReaderAdvanced
title: IWMReaderAdvanced (wmsdkidl.h)
author: windows-sdk-content
description: A call to QueryInterface from a reader object exposes the advanced functionality described in this section.
old-location: wmformat\iwmreaderadvanced.htm
tech.root: wmformat
ms.assetid: a7a20f87-6f21-4fe8-8889-1b6689daf833
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderAdvanced, IWMReaderAdvanced interface [windows Media Format], IWMReaderAdvanced interface [windows Media Format],described, IWMReaderAdvancedInterface, wmformat.iwmreaderadvanced, wmsdkidl/IWMReaderAdvanced
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderAdvanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743469(v=VS.85).aspx">DeliverTime</a>
</td>
<td align="left" width="63%">
Provides the reader with a clock time. This is used only when the application is providing the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743470(v=VS.85).aspx">GetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743471(v=VS.85).aspx">GetAllocateForStream</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743472(v=VS.85).aspx">GetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Ascertains whether manual stream selection has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743473(v=VS.85).aspx">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for output samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743474(v=VS.85).aspx">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743475(v=VS.85).aspx">GetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Retrieves a flag that indicates whether receiving stream selection notifications has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743476(v=VS.85).aspx">GetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to deliver stream samples (compressed samples).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743477(v=VS.85).aspx">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves the current reader statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743478(v=VS.85).aspx">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Ascertains whether a particular stream is currently selected. This can be used only when manual stream selection is specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743479(v=VS.85).aspx">GetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Ascertains whether a user-provided clock has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743480(v=VS.85).aspx">NotifyLateDelivery</a>
</td>
<td align="left" width="63%">
Used to notify the reader that it is delivering data to the application too slowly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743481(v=VS.85).aspx">SetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743482(v=VS.85).aspx">SetAllocateForStream</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743483(v=VS.85).aspx">SetClientInfo</a>
</td>
<td align="left" width="63%">
Sets client-side information used for logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743485(v=VS.85).aspx">SetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Specifies whether stream selection is to be controlled manually.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743486(v=VS.85).aspx">SetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Specifies a flag indicating whether receiving selection callbacks is to be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743487(v=VS.85).aspx">SetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Specifies whether the reader must deliver compressed stream samples to the callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743488(v=VS.85).aspx">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Enables the selected state of a stream to be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743489(v=VS.85).aspx">SetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Specifies that a clock provided by the application is to be used.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757447(v=VS.85).aspx">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757460(v=VS.85).aspx">IWMReaderAdvanced5 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757462(v=VS.85).aspx">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

