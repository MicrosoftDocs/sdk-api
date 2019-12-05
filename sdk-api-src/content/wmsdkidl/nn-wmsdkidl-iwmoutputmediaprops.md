---
UID: NN:wmsdkidl.IWMOutputMediaProps
title: IWMOutputMediaProps (wmsdkidl.h)
description: The IWMOutputMediaProps interface is used to retrieve the properties of an output stream.An IWMOutputMediaProps object is created by a call to IWMReader::GetOutputFormat or IWMReader::GetOutputProps.
old-location: wmformat\iwmoutputmediaprops.htm
tech.root: wmformat
ms.assetid: 8cf40db5-3902-4c14-b728-98da90567e89
ms.date: 12/05/2018
ms.keywords: IWMOutputMediaProps, IWMOutputMediaProps interface [windows Media Format], IWMOutputMediaProps interface [windows Media Format],described, IWMOutputMediaPropsInterface, wmformat.iwmoutputmediaprops, wmsdkidl/IWMOutputMediaProps
ms.topic: interface
f1_keywords:
- wmsdkidl/IWMOutputMediaProps
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
- IWMOutputMediaProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMOutputMediaProps interface


## -description



The <b>IWMOutputMediaProps</b> interface is used to retrieve the properties of an output stream.

An <b>IWMOutputMediaProps</b> object is created by a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat">IWMReader::GetOutputFormat</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMOutputMediaProps</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>. <b>IWMOutputMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMOutputMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmoutputmediaprops-getconnectionname">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the connection to be used for output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmoutputmediaprops-getstreamgroupname">GetStreamGroupName</a>
</td>
<td align="left" width="63%">
Returns an empty string.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/output-media-properties-object">Output Media Properties Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertypenegotiation-tryoutputprops">IWMReaderTypeNegotiation::TryOutputProps</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

