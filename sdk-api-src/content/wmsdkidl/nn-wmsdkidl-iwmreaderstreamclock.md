---
UID: NN:wmsdkidl.IWMReaderStreamClock
title: IWMReaderStreamClock (wmsdkidl.h)
description: The IWMReaderStreamClock interface provides access to the clock used by the reader.This interface exists for every reader object.
helpviewer_keywords: ["IWMReaderStreamClock","IWMReaderStreamClock interface [windows Media Format]","IWMReaderStreamClock interface [windows Media Format]","described","IWMReaderStreamClockInterface","wmformat.iwmreaderstreamclock","wmsdkidl/IWMReaderStreamClock"]
old-location: wmformat\iwmreaderstreamclock.htm
tech.root: wmformat
ms.assetid: 0f170b6d-fd93-4bf8-8a98-f2a80f03b380
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
