---
UID: NN:wmsdkidl.IWMInputMediaProps
title: IWMInputMediaProps (wmsdkidl.h)
description: The IWMInputMediaProps interface is used to retrieve the properties of digital media that will be passed to the writer.An input media properties object is created by a call to either the IWMWriter::GetInputProps or IWMWriter::GetInputFormat method.
helpviewer_keywords: ["IWMInputMediaProps","IWMInputMediaProps interface [windows Media Format]","IWMInputMediaProps interface [windows Media Format]","described","IWMInputMediaPropsInterface","wmformat.iwminputmediaprops","wmsdkidl/IWMInputMediaProps"]
old-location: wmformat\iwminputmediaprops.htm
tech.root: wmformat
ms.assetid: d901ac66-d4b3-4256-bd7b-53cccb3de644
ms.date: 4/26/2023
ms.keywords: IWMInputMediaProps, IWMInputMediaProps interface [windows Media Format], IWMInputMediaProps interface [windows Media Format],described, IWMInputMediaPropsInterface, wmformat.iwminputmediaprops, wmsdkidl/IWMInputMediaProps
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
 - IWMInputMediaProps
 - wmsdkidl/IWMInputMediaProps
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
 - IWMInputMediaProps
---

# IWMInputMediaProps interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMInputMediaProps</b> interface is used to retrieve the properties of digital media that will be passed to the writer.

An input media properties object is created by a call to either the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">IWMWriter::GetInputProps</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">IWMWriter::GetInputFormat</a> method.

## -inheritance

The <b>IWMInputMediaProps</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>. <b>IWMInputMediaProps</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">IWMWriter::GetInputFormat</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">IWMWriter::GetInputProps</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops">IWMWriter::SetInputProps</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
