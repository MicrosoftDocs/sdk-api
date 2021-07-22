---
UID: NN:strmif.IAMOpenProgress
title: IAMOpenProgress (strmif.h)
description: The IAMOpenProgress interface reports the progress of a file-open operation and enables the application to cancel the operation.Filters that open files over a network can expose this interface.
helpviewer_keywords: ["IAMOpenProgress","IAMOpenProgress interface [DirectShow]","IAMOpenProgress interface [DirectShow]","described","IAMOpenProgressInterface","dshow.iamopenprogress","strmif/IAMOpenProgress"]
old-location: dshow\iamopenprogress.htm
tech.root: dshow
ms.assetid: 31021c83-ee83-49c3-a089-31184756fb0d
ms.date: 12/05/2018
ms.keywords: IAMOpenProgress, IAMOpenProgress interface [DirectShow], IAMOpenProgress interface [DirectShow],described, IAMOpenProgressInterface, dshow.iamopenprogress, strmif/IAMOpenProgress
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMOpenProgress
 - strmif/IAMOpenProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMOpenProgress
---

# IAMOpenProgress interface


## -description

The <code>IAMOpenProgress</code> interface reports the progress of a file-open operation and enables the application to cancel the operation.

Filters that open files over a network can expose this interface. An application can use it to query the progress of the download, or to cancel the download. If the network is not responsive, a method such as <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a> might block for an indefinite period. To prevent your application from blocking, create a worker thread that uses <code>IAMOpenProgress</code> to monitor the progress. The worker thread can cancel the operation if a predefined timeout occurs, or in response to a command from the user.

The <a href="/windows/desktop/DirectShow/file-source--url--filter">File Source (URL)</a> filter supports this interface.

## -inheritance

The <b>IAMOpenProgress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMOpenProgress</b> also has these types of members:

