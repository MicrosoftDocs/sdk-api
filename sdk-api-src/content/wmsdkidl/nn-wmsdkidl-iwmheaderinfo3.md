---
UID: NN:wmsdkidl.IWMHeaderInfo3
title: IWMHeaderInfo3 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMHeaderInfo3 interface supports the following new metadata features:Attribute data in excess of 64 kilobytes.Multiple attributes with the same name.Attributes in multiple languages.Because the attributes created using this interface can have duplicate names, the methods of this interface use index values to identify attributes.The IWMHeaderInfo3 interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the QueryInterface method of any other interface in the desired object.
old-location: wmformat\iwmheaderinfo3.htm
tech.root: wmformat
ms.assetid: 5791e330-3877-4d3a-b27f-f14b97d1a435
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMHeaderInfo3, IWMHeaderInfo3 interface [windows Media Format], IWMHeaderInfo3 interface [windows Media Format],described, IWMHeaderInfo3Interface, wmformat.iwmheaderinfo3, wmsdkidl/IWMHeaderInfo3
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMHeaderInfo3"
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
 - IWMHeaderInfo3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMHeaderInfo3 interface


## -description



The <b>IWMHeaderInfo3</b> interface supports the following new metadata features:

<ul>
<li>Attribute data in excess of 64 kilobytes.</li>
<li>Multiple attributes with the same name.</li>
<li>Attributes in multiple languages.</li>
</ul>
Because the attributes created using this interface can have duplicate names, the methods of this interface use index values to identify attributes.

The <b>IWMHeaderInfo3</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMHeaderInfo3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>. <b>IWMHeaderInfo3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMHeaderInfo3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute">AddAttribute</a>
</td>
<td align="left" width="63%">
Adds an attribute for a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo">AddCodecInfo</a>
</td>
<td align="left" width="63%">
Adds information about a codec that was used to compress data in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute">DeleteAttribute</a>
</td>
<td align="left" width="63%">
Deletes an attribute using the attribute index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex">GetAttributeByIndexEx</a>
</td>
<td align="left" width="63%">
Retrieves an attribute by its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributecountex">GetAttributeCountEx</a>
</td>
<td align="left" width="63%">
Retrieves the total number of attributes in the file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices">GetAttributeIndices</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the indices of attributes for a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute">ModifyAttribute</a>
</td>
<td align="left" width="63%">
Changes the settings of an existing attribute.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



For information about using the writer for metadata editing, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/to-edit-metadata-with-the-writer">To Edit Metadata with the Writer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

