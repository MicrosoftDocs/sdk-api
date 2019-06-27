---
UID: NN:wmsdkidl.IWMReaderAdvanced
title: IWMReaderAdvanced (wmsdkidl.h)
author: windows-sdk-content
description: A call to QueryInterface from a reader object exposes the advanced functionality described in this section.
old-location: wmformat\iwmreaderadvanced.htm
tech.root: wmformat
ms.assetid: a7a20f87-6f21-4fe8-8889-1b6689daf833
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced, IWMReaderAdvanced interface [windows Media Format], IWMReaderAdvanced interface [windows Media Format],described, IWMReaderAdvancedInterface, wmformat.iwmreaderadvanced, wmsdkidl/IWMReaderAdvanced
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMReaderAdvanced"
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
ms.custom: 19H1
---

# IWMReaderAdvanced interface


## -description



A call to <b>QueryInterface</b> from a reader object exposes the advanced functionality described in this section.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderAdvanced</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime">DeliverTime</a>
</td>
<td align="left" width="63%">
Provides the reader with a clock time. This is used only when the application is providing the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getallocateforoutput">GetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getallocateforstream">GetAllocateForStream</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to use the <b>IWMReaderCallbackAdvanced</b> interface to allocate buffers for a particular stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmanualstreamselection">GetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Ascertains whether manual stream selection has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for output samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getreceiveselectioncallbacks">GetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Retrieves a flag that indicates whether receiving stream selection notifications has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getreceivestreamsamples">GetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether the reader is configured to deliver stream samples (compressed samples).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves the current reader statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Ascertains whether a particular stream is currently selected. This can be used only when manual stream selection is specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getuserprovidedclock">GetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Ascertains whether a user-provided clock has been specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-notifylatedelivery">NotifyLateDelivery</a>
</td>
<td align="left" width="63%">
Used to notify the reader that it is delivering data to the application too slowly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput">SetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream">SetAllocateForStream</a>
</td>
<td align="left" width="63%">
Specifies whether to allocate buffers from the user-supplied callback, or internally, for stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo">SetClientInfo</a>
</td>
<td align="left" width="63%">
Sets client-side information used for logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection">SetManualStreamSelection</a>
</td>
<td align="left" width="63%">
Specifies whether stream selection is to be controlled manually.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceiveselectioncallbacks">SetReceiveSelectionCallbacks</a>
</td>
<td align="left" width="63%">
Specifies a flag indicating whether receiving selection callbacks is to be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples">SetReceiveStreamSamples</a>
</td>
<td align="left" width="63%">
Specifies whether the reader must deliver compressed stream samples to the callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Enables the selected state of a stream to be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock">SetUserProvidedClock</a>
</td>
<td align="left" width="63%">
Specifies that a clock provided by the application is to be used.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
 

 

