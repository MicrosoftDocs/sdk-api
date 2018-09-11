---
UID: NN:wmsdkidl.IWMReaderTimecode
title: IWMReaderTimecode
author: windows-sdk-content
description: The IWMReaderTimecode interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges.
old-location: wmformat\iwmreadertimecode.htm
tech.root: wmformat
ms.assetid: 7f7d5608-c505-46ab-9e1e-e45b383c879b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderTimecode, IWMReaderTimecode interface [windows Media Format], IWMReaderTimecode interface [windows Media Format],described, IWMReaderTimecodeInterface, wmformat.iwmreadertimecode, wmsdkidl/IWMReaderTimecode
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMReaderTimecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderTimecode interface


## -description



The <b>IWMReaderTimecode</b> interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges. A range of SMPTE time code is a series of samples with time codes that are contiguous and in increasing order. An individual video stream can contain more than one range.

An <b>IWMReaderTimecode</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderTimecode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderTimecode</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5bc1f21c-0aca-4e45-ac82-898cb8b9f4cc">GetTimecodeRangeBounds</a>
</td>
<td align="left" width="63%">
Retrieves the starting and ending time codes for a specified SMPTE time code range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df58f968-23f8-407b-b18c-569732635464">GetTimecodeRangeCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of SMPTE time code ranges for a specified stream.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

