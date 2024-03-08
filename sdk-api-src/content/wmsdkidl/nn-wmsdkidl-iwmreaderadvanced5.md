---
UID: NN:wmsdkidl.IWMReaderAdvanced5
title: IWMReaderAdvanced5 (wmsdkidl.h)
description: The IWMReaderAdvanced5 interface enables you to associate a player-hook callback interface with the reader object.An IWMReaderAdvanced5 interface exists for every reader object.
helpviewer_keywords: ["IWMReaderAdvanced5","IWMReaderAdvanced5 interface [windows Media Format]","IWMReaderAdvanced5 interface [windows Media Format]","described","IWMReaderAdvanced5Interface","wmformat.iwmreaderadvanced5","wmsdkidl/IWMReaderAdvanced5"]
old-location: wmformat\iwmreaderadvanced5.htm
tech.root: wmformat
ms.assetid: 28d697d8-99b5-4968-a765-ba01b86914f6
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced5, IWMReaderAdvanced5 interface [windows Media Format], IWMReaderAdvanced5 interface [windows Media Format],described, IWMReaderAdvanced5Interface, wmformat.iwmreaderadvanced5, wmsdkidl/IWMReaderAdvanced5
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
 - IWMReaderAdvanced5
 - wmsdkidl/IWMReaderAdvanced5
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
 - IWMReaderAdvanced5
---

# IWMReaderAdvanced5 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderAdvanced5</b> interface enables you to associate a player-hook callback interface with the reader object.

An <b>IWMReaderAdvanced5</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.

## -inheritance

The <b>IWMReaderAdvanced5</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4</a>. <b>IWMReaderAdvanced5</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

A player-hook callback can be assigned in the reader object to enable per-sample processing when using DirectX Video Acceleration.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
