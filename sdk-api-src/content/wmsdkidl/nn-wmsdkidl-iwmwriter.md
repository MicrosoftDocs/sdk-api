---
UID: NN:wmsdkidl.IWMWriter
title: IWMWriter (wmsdkidl.h)
description: The IWMWriter interface is used to write ASF files.
helpviewer_keywords: ["IWMWriter","IWMWriter interface [windows Media Format]","IWMWriter interface [windows Media Format]","described","IWMWriterInterface","wmformat.iwmwriter","wmsdkidl/IWMWriter"]
old-location: wmformat\iwmwriter.htm
tech.root: wmformat
ms.assetid: a194ef11-5203-4e85-af91-cdce0c53fe76
ms.date: 12/05/2018
ms.keywords: IWMWriter, IWMWriter interface [windows Media Format], IWMWriter interface [windows Media Format],described, IWMWriterInterface, wmformat.iwmwriter, wmsdkidl/IWMWriter
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
 - IWMWriter
 - wmsdkidl/IWMWriter
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
 - IWMWriter
---

# IWMWriter interface


## -description

The <b>IWMWriter</b> interface is used to write ASF files. It includes methods for allocating buffers, setting and retrieving input properties, and setting profiles and output file names. The writer object exposes this interface. To create the writer object, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriter">WMCreateWriter</a> function.

## -inheritance

The <b>IWMWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
