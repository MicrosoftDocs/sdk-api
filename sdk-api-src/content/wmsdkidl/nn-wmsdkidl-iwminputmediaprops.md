---
UID: NN:wmsdkidl.IWMInputMediaProps
title: IWMInputMediaProps (wmsdkidl.h)
author: windows-sdk-content
description: The IWMInputMediaProps interface is used to retrieve the properties of digital media that will be passed to the writer.An input media properties object is created by a call to either the IWMWriter::GetInputProps or IWMWriter::GetInputFormat method.
old-location: wmformat\iwminputmediaprops.htm
tech.root: wmformat
ms.assetid: d901ac66-d4b3-4256-bd7b-53cccb3de644
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMInputMediaProps, IWMInputMediaProps interface [windows Media Format], IWMInputMediaProps interface [windows Media Format],described, IWMInputMediaPropsInterface, wmformat.iwminputmediaprops, wmsdkidl/IWMInputMediaProps
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMInputMediaProps"
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
 - IWMInputMediaProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMInputMediaProps interface


## -description



The <b>IWMInputMediaProps</b> interface is used to retrieve the properties of digital media that will be passed to the writer.

An input media properties object is created by a call to either the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">IWMWriter::GetInputProps</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">IWMWriter::GetInputFormat</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMInputMediaProps</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>. <b>IWMInputMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMInputMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the connection name specified in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getgroupname">GetGroupName</a>
</td>
<td align="left" width="63%">
Not implemented in this release. Returns an empty string.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/input-media-properties-object">Input Media Properties Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">IWMWriter::GetInputFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">IWMWriter::GetInputProps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops">IWMWriter::SetInputProps</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

