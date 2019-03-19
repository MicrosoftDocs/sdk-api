---
UID: NN:wmsdkidl.IWMHeaderInfo2
title: IWMHeaderInfo2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMHeaderInfo2 interface exposes information about the codecs used to create the content in a file.The IWMHeaderInfo2 interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object.
old-location: wmformat\iwmheaderinfo2.htm
tech.root: wmformat
ms.assetid: af670b54-f695-4b6f-8190-c25ea409b53a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMHeaderInfo2, IWMHeaderInfo2 interface [windows Media Format], IWMHeaderInfo2 interface [windows Media Format],described, IWMHeaderInfo2Interface, wmformat.iwmheaderinfo2, wmsdkidl/IWMHeaderInfo2
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
 - IWMHeaderInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMHeaderInfo2 interface


## -description



The <b>IWMHeaderInfo2</b> interface exposes information about the <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">codecs</a> used to create the content in a file.

The <b>IWMHeaderInfo2</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMHeaderInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd798504(v=VS.85).aspx">IWMHeaderInfo</a>. <b>IWMHeaderInfo2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798506(v=VS.85).aspx">GetCodecInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798507(v=VS.85).aspx">GetCodecInfoCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of codecs for which information is available.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



For information about using the writer for metadata editing, see <a href="https://msdn.microsoft.com/86badfe3-64bc-4285-a231-f6c0ebf4f262">To Edit Metadata with the Writer</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798504(v=VS.85).aspx">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798508(v=VS.85).aspx">IWMHeaderInfo3 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

