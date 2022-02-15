---
UID: NN:wmsdkidl.IWMReaderCallback
title: IWMReaderCallback (wmsdkidl.h)
description: The IWMReaderCallback is implemented by the application to handle data being read from a file. A pointer to the interface is passed to IWMReader::Open.
helpviewer_keywords: ["IWMReaderCallback","IWMReaderCallback interface [windows Media Format]","IWMReaderCallback interface [windows Media Format]","described","IWMReaderCallbackInterface","wmformat.iwmreadercallback","wmsdkidl/IWMReaderCallback"]
old-location: wmformat\iwmreadercallback.htm
tech.root: wmformat
ms.assetid: 69b897a8-cc26-445d-9d41-b917b399fb14
ms.date: 12/05/2018
ms.keywords: IWMReaderCallback, IWMReaderCallback interface [windows Media Format], IWMReaderCallback interface [windows Media Format],described, IWMReaderCallbackInterface, wmformat.iwmreadercallback, wmsdkidl/IWMReaderCallback
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
 - IWMReaderCallback
 - wmsdkidl/IWMReaderCallback
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
 - IWMReaderCallback
---

# IWMReaderCallback interface


## -description

The <b>IWMReaderCallback</b> is implemented by the application to handle data being read from a file. A pointer to the interface is passed to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>.

## -inheritance

The <b>IWMReaderCallback</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a>. <b>IWMReaderCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
