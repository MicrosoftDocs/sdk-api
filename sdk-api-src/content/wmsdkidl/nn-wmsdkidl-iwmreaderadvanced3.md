---
UID: NN:wmsdkidl.IWMReaderAdvanced3
title: IWMReaderAdvanced3 (wmsdkidl.h)
description: The IWMReaderAdvanced3 interface provides additional functionality to the reader object.helpviewer_keywords: ["IWMReaderAdvanced3","IWMReaderAdvanced3 interface [windows Media Format]","IWMReaderAdvanced3 interface [windows Media Format]","described","IWMReaderAdvanced3Interface","wmformat.iwmreaderadvanced3","wmsdkidl/IWMReaderAdvanced3"]
old-location: wmformat\iwmreaderadvanced3.htm
tech.root: wmformat
ms.assetid: 20bf3c00-0f35-4b8e-b78d-a36fbfd865b7
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced3, IWMReaderAdvanced3 interface [windows Media Format], IWMReaderAdvanced3 interface [windows Media Format],described, IWMReaderAdvanced3Interface, wmformat.iwmreaderadvanced3, wmsdkidl/IWMReaderAdvanced3
f1_keywords:
- wmsdkidl/IWMReaderAdvanced3
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
- IWMReaderAdvanced3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced3 interface


## -description



The <b>IWMReaderAdvanced3</b> interface provides additional functionality to the reader object. It contains methods that enhance the ability to playback a file.

<b>IWMReaderAdvanced3</b> exists for each instance of the reader objects created with the <b>WMCreateReader</b> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2</a>. <b>IWMReaderAdvanced3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition">StartAtPosition</a>
</td>
<td align="left" width="63%">
Provides the ability to specify a starting position using a variety of offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-stopnetstreaming">StopNetStreaming</a>
</td>
<td align="left" width="63%">
Stops network streaming while received packets continue to be delivered.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
 

 

