---
UID: NN:wmsdkidl.IWMWriterAdvanced3
title: IWMWriterAdvanced3 (wmsdkidl.h)
description: The IWMWriterAdvanced3 interface provides additional functionality for the writer object.IWMWriterAdvanced3 exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced3.htm
tech.root: wmformat
ms.assetid: 99f7e4f7-0080-498d-b4f1-960c4955b4db
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced3, IWMWriterAdvanced3 interface [windows Media Format], IWMWriterAdvanced3 interface [windows Media Format],described, IWMWriterAdvanced3Interface, wmformat.iwmwriteradvanced3, wmsdkidl/IWMWriterAdvanced3
ms.topic: interface
f1_keywords:
- wmsdkidl/IWMWriterAdvanced3
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
- IWMWriterAdvanced3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced3 interface


## -description



The <b>IWMWriterAdvanced3</b> interface provides additional functionality for the writer object.

<b>IWMWriterAdvanced3</b> exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2</a>. <b>IWMWriterAdvanced3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterAdvanced3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex">GetStatisticsEx</a>
</td>
<td align="left" width="63%">
Retrieves extended statistics for the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-setnonblocking">SetNonBlocking</a>
</td>
<td align="left" width="63%">
Configures the writer so that it does not block the calling thread.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
 

 

