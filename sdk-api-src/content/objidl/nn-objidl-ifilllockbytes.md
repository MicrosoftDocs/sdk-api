---
UID: NN:objidl.IFillLockBytes
title: IFillLockBytes (objidl.h)
description: The IFillLockBytes interface enables downloading code to write data asynchronously to a structured storage byte array.
helpviewer_keywords: ["IFillLockBytes","IFillLockBytes interface [Structured Storage]","IFillLockBytes interface [Structured Storage]","described","_stg_ifilllockbytes","objidl/IFillLockBytes","stg.ifilllockbytes"]
old-location: stg\ifilllockbytes.htm
tech.root: Stg
ms.assetid: 033b3db4-3ff0-4cb4-916f-2490e92f5e6a
ms.date: 12/05/2018
ms.keywords: IFillLockBytes, IFillLockBytes interface [Structured Storage], IFillLockBytes interface [Structured Storage],described, _stg_ifilllockbytes, objidl/IFillLockBytes, stg.ifilllockbytes
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFillLockBytes
 - objidl/IFillLockBytes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IFillLockBytes
---

# IFillLockBytes interface


## -description

The 
<b>IFillLockBytes</b> interface enables downloading code to write data asynchronously to a structured storage byte array. When the downloading code has new data available, it calls 
<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a> or <a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillat">IFillLockBytes::FillAt</a> to write the data to the byte array. An application attempting to access this data, through calls to the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface, can do so even as the downloader continues to make calls to 
<b>IFillLockBytes</b>. If the application attempts to access data that has not already been downloaded through a call to 
<b>IFillLockBytes</b>, then 
<b>ILockBytes</b> returns a new error, E_PENDING.

## -inheritance

The <b>IFillLockBytes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFillLockBytes</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774966(v=vs.85)">BINDINFO</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iprogressnotify">IProgressNotify</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
