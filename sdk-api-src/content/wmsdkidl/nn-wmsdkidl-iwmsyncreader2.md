---
UID: NN:wmsdkidl.IWMSyncReader2
title: IWMSyncReader2 (wmsdkidl.h)
description: The IWMSyncReader2 interface provides advanced features for the synchronous reader.
helpviewer_keywords: ["IWMSyncReader2","IWMSyncReader2 interface [windows Media Format]","IWMSyncReader2 interface [windows Media Format]","described","IWMSyncReader2Interface","wmformat.iwmsyncreader2","wmsdkidl/IWMSyncReader2"]
old-location: wmformat\iwmsyncreader2.htm
tech.root: wmformat
ms.assetid: f3db7530-a662-46f1-bc64-1dd4523dc87c
ms.date: 12/05/2018
ms.keywords: IWMSyncReader2, IWMSyncReader2 interface [windows Media Format], IWMSyncReader2 interface [windows Media Format],described, IWMSyncReader2Interface, wmformat.iwmsyncreader2, wmsdkidl/IWMSyncReader2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSyncReader2
 - wmsdkidl/IWMSyncReader2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMSyncReader2
---

# IWMSyncReader2 interface


## -description

The <b>IWMSyncReader2</b> interface provides advanced features for the synchronous reader. It contains methods for allocating samples manually and for seeking to SMPTE time codes.

An <b>IWMSyncReader2</b> interface exists for every synchronous reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the synchronous reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSyncReader2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader</a>. <b>IWMSyncReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSyncReader2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-getallocateforoutput">GetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMReaderAllocatorEx</b> interface for allocating output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-getallocateforstream">GetAllocateForStream</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMReaderAllocatorEx</b> interface for allocating stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput">SetAllocateForOutput</a>
</td>
<td align="left" width="63%">
Sets an <b>IWMReaderAllocatorEx</b> interface for allocating output samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream">SetAllocateForStream</a>
</td>
<td align="left" width="63%">
Sets an <b>IWMReaderAllocatorEx</b> interface for allocating stream samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebyframeex">SetRangeByFrameEx</a>
</td>
<td align="left" width="63%">
Enables you to play a portion of a file specified by frame numbers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode">SetRangeByTimecode</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback using SMPTE time codes.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by calling the QueryInterface method of this interface, see <a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>