---
UID: NN:wmsdkidl.IWMHeaderInfo2
title: IWMHeaderInfo2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMHeaderInfo2 interface exposes information about the codecs used to create the content in a file.The IWMHeaderInfo2 interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object.
old-location: wmformat\iwmheaderinfo2.htm
tech.root: wmformat
ms.assetid: af670b54-f695-4b6f-8190-c25ea409b53a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMHeaderInfo2, IWMHeaderInfo2 interface [windows Media Format], IWMHeaderInfo2 interface [windows Media Format],described, IWMHeaderInfo2Interface, wmformat.iwmheaderinfo2, wmsdkidl/IWMHeaderInfo2
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMHeaderInfo2"
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
 - IWMHeaderInfo2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMHeaderInfo2 interface


## -description



The <b>IWMHeaderInfo2</b> interface exposes information about the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">codecs</a> used to create the content in a file.

The <b>IWMHeaderInfo2</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMHeaderInfo2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo</a>. <b>IWMHeaderInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMHeaderInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo">GetCodecInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount">GetCodecInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of codecs for which information is available.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



For information about using the writer for metadata editing, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/to-edit-metadata-with-the-writer">To Edit Metadata with the Writer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

