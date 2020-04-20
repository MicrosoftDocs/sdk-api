---
UID: NN:wmsdkidl.IWMReaderAdvanced6
title: IWMReaderAdvanced6 (wmsdkidl.h)
description: The IWMReaderAdvanced6 interface enables sample protection.An IWMReaderAdvanced6 interface exists for every reader object.helpviewer_keywords: ["IWMReaderAdvanced6","IWMReaderAdvanced6 interface [windows Media Format]","IWMReaderAdvanced6 interface [windows Media Format]","described","IWMReaderAdvanced6Interface","wmformat.iwmreaderadvanced6","wmsdkidl/IWMReaderAdvanced6"]
old-location: wmformat\iwmreaderadvanced6.htm
tech.root: wmformat
ms.assetid: 95e8c151-9aae-4930-824c-8809dfc07705
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced6, IWMReaderAdvanced6 interface [windows Media Format], IWMReaderAdvanced6 interface [windows Media Format],described, IWMReaderAdvanced6Interface, wmformat.iwmreaderadvanced6, wmsdkidl/IWMReaderAdvanced6
f1_keywords:
- wmsdkidl/IWMReaderAdvanced6
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
- IWMReaderAdvanced6
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced6 interface


## -description



The <b>IWMReaderAdvanced6</b> interface enables sample protection.

An <b>IWMReaderAdvanced6</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced6</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5</a>. <b>IWMReaderAdvanced6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced6-setprotectstreamsamples">SetProtectStreamSamples</a>
</td>
<td align="left" width="63%">
Configures sample protection.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

