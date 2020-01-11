---
UID: NN:wmsdkidl.IWMReaderCallbackAdvanced
title: IWMReaderCallbackAdvanced (wmsdkidl.h)
description: The IWMReaderCallback interface is implemented by the application to handle data being read from a file.
old-location: wmformat\iwmreadercallbackadvanced.htm
tech.root: wmformat
ms.assetid: 9d18961a-5ea4-4f3e-b473-7399e155f800
ms.date: 12/05/2018
ms.keywords: IWMReaderCallbackAdvanced, IWMReaderCallbackAdvanced interface [windows Media Format], IWMReaderCallbackAdvanced interface [windows Media Format],described, IWMReaderCallbackAdvancedInterface, wmformat.iwmreadercallbackadvanced, wmsdkidl/IWMReaderCallbackAdvanced
f1_keywords:
- wmsdkidl/IWMReaderCallbackAdvanced
dev_langs:
- c++
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
- IWMReaderCallbackAdvanced
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderCallbackAdvanced interface


## -description



The <b>IWMReaderCallback</b> interface is implemented by the application to handle data being read from a file.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderCallbackAdvanced</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderCallbackAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderCallbackAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforoutput">AllocateForOutput</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforstream">AllocateForStream</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">OnStreamSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onoutputpropschanged">OnOutputPropsChanged</a>
</td>
<td align="left" width="63%">
Called when the output media properties change because of an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">OnStreamSample</a>
</td>
<td align="left" width="63%">
Delivers stream samples from the source file without decompressing them first.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamselection">OnStreamSelection</a>
</td>
<td align="left" width="63%">
Notifies the application of stream changes made due to bandwidth restrictions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime">OnTime</a>
</td>
<td align="left" width="63%">
Notifies the application of the clock time the reader is working to. This is used when a user-provided clock has been specified.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
 

 

