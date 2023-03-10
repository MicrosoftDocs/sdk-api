---
UID: NN:wmsdkidl.IWMReaderStreamClock
title: IWMReaderStreamClock (wmsdkidl.h)
description: The IWMReaderStreamClock interface provides access to the clock used by the reader.This interface exists for every reader object.
helpviewer_keywords: ["IWMReaderStreamClock","IWMReaderStreamClock interface [windows Media Format]","IWMReaderStreamClock interface [windows Media Format]","described","IWMReaderStreamClockInterface","wmformat.iwmreaderstreamclock","wmsdkidl/IWMReaderStreamClock"]
old-location: wmformat\iwmreaderstreamclock.htm
tech.root: wmformat
ms.assetid: 0f170b6d-fd93-4bf8-8a98-f2a80f03b380
ms.date: 12/05/2018
ms.keywords: IWMReaderStreamClock, IWMReaderStreamClock interface [windows Media Format], IWMReaderStreamClock interface [windows Media Format],described, IWMReaderStreamClockInterface, wmformat.iwmreaderstreamclock, wmsdkidl/IWMReaderStreamClock
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
 - IWMReaderStreamClock
 - wmsdkidl/IWMReaderStreamClock
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
 - IWMReaderStreamClock
---

# IWMReaderStreamClock interface


## -description

The <b>IWMReaderStreamClock</b> interface provides access to the clock used by the reader.

This interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMReaderStreamClock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderStreamClock</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
