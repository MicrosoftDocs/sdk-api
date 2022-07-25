---
UID: NN:wmsdkidl.IWMReader
title: IWMReader (wmsdkidl.h)
description: The IWMReader interface is used to open, close, start, pause, resume, and unlock the WMReader object.
helpviewer_keywords: ["IWMReader","IWMReader interface [windows Media Format]","IWMReader interface [windows Media Format]","described","IWMReaderInterface","wmformat.iwmreader","wmsdkidl/IWMReader"]
old-location: wmformat\iwmreader.htm
tech.root: wmformat
ms.assetid: e995b707-d388-4ec3-b3c8-b111628c13d7
ms.date: 12/05/2018
ms.keywords: IWMReader, IWMReader interface [windows Media Format], IWMReader interface [windows Media Format],described, IWMReaderInterface, wmformat.iwmreader, wmsdkidl/IWMReader
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
 - IWMReader
 - wmsdkidl/IWMReader
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
 - IWMReader
---

# IWMReader interface


## -description

The <b>IWMReader</b> interface is used to open, close, start, pause, resume, and unlock the <b>WMReader</b> object. It is also used to stop reading files, and to get and set the output properties.

Many of the methods in this interface are asynchronous and send status notifications to the application through an <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method implemented in the application.

## -inheritance

The <b>IWMReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
