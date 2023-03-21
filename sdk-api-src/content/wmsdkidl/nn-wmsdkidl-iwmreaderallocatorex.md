---
UID: NN:wmsdkidl.IWMReaderAllocatorEx
title: IWMReaderAllocatorEx (wmsdkidl.h)
description: The IWMReaderAllocatorEx interface provides expanded alternatives to the AllocateForOutput and AllocateForStream methods of the IWMReaderCallbackAdvanced interface.
helpviewer_keywords: ["IWMReaderAllocatorEx","IWMReaderAllocatorEx interface [windows Media Format]","IWMReaderAllocatorEx interface [windows Media Format]","described","IWMReaderAllocatorExInterface","wmformat.iwmreaderallocatorex","wmsdkidl/IWMReaderAllocatorEx"]
old-location: wmformat\iwmreaderallocatorex.htm
tech.root: wmformat
ms.assetid: be727c7b-b252-44db-825b-5c683e551fd2
ms.date: 12/05/2018
ms.keywords: IWMReaderAllocatorEx, IWMReaderAllocatorEx interface [windows Media Format], IWMReaderAllocatorEx interface [windows Media Format],described, IWMReaderAllocatorExInterface, wmformat.iwmreaderallocatorex, wmsdkidl/IWMReaderAllocatorEx
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
 - IWMReaderAllocatorEx
 - wmsdkidl/IWMReaderAllocatorEx
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
 - IWMReaderAllocatorEx
---

# IWMReaderAllocatorEx interface


## -description

The <b>IWMReaderAllocatorEx</b> interface provides expanded alternatives to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforoutput">AllocateForOutput</a> and <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforstream">AllocateForStream</a> methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a> interface. This interface is implemented by the application, which passes this interface pointer to the synchronous reader object by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream">IWMSyncReader2::SetAllocateForStream</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput">SetAllocateForOutput</a>.

## -inheritance

The <b>IWMReaderAllocatorEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderAllocatorEx</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/allocating-buffers-for-file-reading">Allocating Buffers for File Reading</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
