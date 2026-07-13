---
UID: NN:wmsdkidl.IWMSyncReader2
title: IWMSyncReader2 (wmsdkidl.h)
description: The IWMSyncReader2 interface provides advanced features for the synchronous reader.
helpviewer_keywords: ["IWMSyncReader2","IWMSyncReader2 interface [windows Media Format]","IWMSyncReader2 interface [windows Media Format]","described","IWMSyncReader2Interface","wmformat.iwmsyncreader2","wmsdkidl/IWMSyncReader2"]
old-location: wmformat\iwmsyncreader2.htm
tech.root: wmformat
ms.assetid: f3db7530-a662-46f1-bc64-1dd4523dc87c
ms.date: 4/26/2023
ms.keywords: IWMSyncReader2, IWMSyncReader2 interface [windows Media Format], IWMSyncReader2 interface [windows Media Format],described, IWMSyncReader2Interface, wmformat.iwmsyncreader2, wmsdkidl/IWMSyncReader2
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
 - IWMSyncReader2
 - wmsdkidl/IWMSyncReader2
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
 - IWMSyncReader2
---

# IWMSyncReader2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMSyncReader2</b> interface provides advanced features for the synchronous reader. It contains methods for allocating samples manually and for seeking to SMPTE time codes.

An <b>IWMSyncReader2</b> interface exists for every synchronous reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the synchronous reader object.

## -inheritance

The <b>IWMSyncReader2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader</a>. <b>IWMSyncReader2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
