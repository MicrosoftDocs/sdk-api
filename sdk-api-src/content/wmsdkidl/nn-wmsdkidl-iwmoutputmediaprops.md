---
UID: NN:wmsdkidl.IWMOutputMediaProps
title: IWMOutputMediaProps (wmsdkidl.h)
description: The IWMOutputMediaProps interface is used to retrieve the properties of an output stream.An IWMOutputMediaProps object is created by a call to IWMReader::GetOutputFormat or IWMReader::GetOutputProps.
helpviewer_keywords: ["IWMOutputMediaProps","IWMOutputMediaProps interface [windows Media Format]","IWMOutputMediaProps interface [windows Media Format]","described","IWMOutputMediaPropsInterface","wmformat.iwmoutputmediaprops","wmsdkidl/IWMOutputMediaProps"]
old-location: wmformat\iwmoutputmediaprops.htm
tech.root: wmformat
ms.assetid: 8cf40db5-3902-4c14-b728-98da90567e89
ms.date: 4/26/2023
ms.keywords: IWMOutputMediaProps, IWMOutputMediaProps interface [windows Media Format], IWMOutputMediaProps interface [windows Media Format],described, IWMOutputMediaPropsInterface, wmformat.iwmoutputmediaprops, wmsdkidl/IWMOutputMediaProps
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMOutputMediaProps
 - wmsdkidl/IWMOutputMediaProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMOutputMediaProps
---

# IWMOutputMediaProps interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMOutputMediaProps</b> interface is used to retrieve the properties of an output stream.

An <b>IWMOutputMediaProps</b> object is created by a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat">IWMReader::GetOutputFormat</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a>.

## -inheritance

The <b>IWMOutputMediaProps</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>. <b>IWMOutputMediaProps</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertypenegotiation-tryoutputprops">IWMReaderTypeNegotiation::TryOutputProps</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
