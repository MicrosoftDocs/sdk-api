---
UID: NN:wmsdkidl.IWMHeaderInfo3
title: IWMHeaderInfo3
author: windows-sdk-content
description: The IWMHeaderInfo3 interface supports the following new metadata features:Attribute data in excess of 64 kilobytes.Multiple attributes with the same name.Attributes in multiple languages.Because the attributes created using this interface can have duplicate names, the methods of this interface use index values to identify attributes.The IWMHeaderInfo3 interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the QueryInterface method of any other interface in the desired object.
old-location: wmformat\iwmheaderinfo3.htm
tech.root: wmformat
ms.assetid: 5791e330-3877-4d3a-b27f-f14b97d1a435
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMHeaderInfo3, IWMHeaderInfo3 interface [windows Media Format], IWMHeaderInfo3 interface [windows Media Format],described, IWMHeaderInfo3Interface, wmformat.iwmheaderinfo3, wmsdkidl/IWMHeaderInfo3
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMHeaderInfo3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMHeaderInfo3</b> interface inherits from <a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>. <b>IWMHeaderInfo3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/15ecb34d-f70d-43a3-b369-2d9c2532945e">AddAttribute</a>
</td>
<td align="left" width="63%">
Adds an attribute for a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c5bc019-e4bb-419b-91ce-779fd36d7b4c">AddCodecInfo</a>
</td>
<td align="left" width="63%">
Adds information about a codec that was used to compress data in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a69da90f-c8c5-4bf7-a1d8-7031aa9d1704">DeleteAttribute</a>
</td>
<td align="left" width="63%">
Deletes an attribute using the attribute index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c20f4c79-f5b3-45d9-ad70-5fb9745bbf1b">GetAttributeByIndexEx</a>
</td>
<td align="left" width="63%">
Retrieves an attribute by its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c56d7b6-4f59-450e-938c-b7d0bd37ea08">GetAttributeCountEx</a>
</td>
<td align="left" width="63%">
Retrieves the total number of attributes in the file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15c8f0c2-f2d4-441a-b6a9-774da820d03c">GetAttributeIndices</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the indices of attributes for a specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/503099e9-a1a9-406f-abc9-7c632d757cca">ModifyAttribute</a>
</td>
<td align="left" width="63%">
Changes the settings of an existing attribute.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



For information about using the writer for metadata editing, see <a href="https://msdn.microsoft.com/86badfe3-64bc-4285-a231-f6c0ebf4f262">To Edit Metadata with the Writer</a>.




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

