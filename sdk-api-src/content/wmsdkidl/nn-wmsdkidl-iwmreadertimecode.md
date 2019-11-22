---
UID: NN:wmsdkidl.IWMReaderTimecode
title: IWMReaderTimecode (wmsdkidl.h)

description: The IWMReaderTimecode interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges.
old-location: wmformat\iwmreadertimecode.htm
tech.root: wmformat
ms.assetid: 7f7d5608-c505-46ab-9e1e-e45b383c879b

ms.date: 12/05/2018
ms.keywords: IWMReaderTimecode, IWMReaderTimecode interface [windows Media Format], IWMReaderTimecode interface [windows Media Format],described, IWMReaderTimecodeInterface, wmformat.iwmreadertimecode, wmsdkidl/IWMReaderTimecode
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMReaderTimecode"
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
 - IWMReaderTimecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderTimecode interface


## -description



The <b>IWMReaderTimecode</b> interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges. A range of SMPTE time code is a series of samples with time codes that are contiguous and in increasing order. An individual video stream can contain more than one range.

An <b>IWMReaderTimecode</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderTimecode</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderTimecode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderTimecode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertimecode-gettimecoderangebounds">GetTimecodeRangeBounds</a>
</td>
<td align="left" width="63%">
Retrieves the starting and ending time codes for a specified SMPTE time code range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertimecode-gettimecoderangecount">GetTimecodeRangeCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of SMPTE time code ranges for a specified stream.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>
 

 

