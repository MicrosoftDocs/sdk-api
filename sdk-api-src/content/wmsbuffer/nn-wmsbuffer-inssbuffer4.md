---
UID: NN:wmsbuffer.INSSBuffer4
title: INSSBuffer4 (wmsbuffer.h)
description: The INSSBuffer4 interface provides methods to enumerate buffer properties.
helpviewer_keywords: ["INSSBuffer4","INSSBuffer4 interface [windows Media Format]","INSSBuffer4 interface [windows Media Format]","described","INSSBuffer4Interface","wmformat.inssbuffer4","wmsbuffer/INSSBuffer4"]
old-location: wmformat\inssbuffer4.htm
tech.root: wmformat
ms.assetid: d6531e52-b58b-46ed-a47b-444cd98e1ec5
ms.date: 4/26/2023
ms.keywords: INSSBuffer4, INSSBuffer4 interface [windows Media Format], INSSBuffer4 interface [windows Media Format],described, INSSBuffer4Interface, wmformat.inssbuffer4, wmsbuffer/INSSBuffer4
req.header: wmsbuffer.h
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
 - INSSBuffer4
 - wmsbuffer/INSSBuffer4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsbuffer.h
api_name:
 - INSSBuffer4
---

# INSSBuffer4 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>INSSBuffer4</b> interface provides methods to enumerate buffer properties. These methods are important when reading files that may have properties of which you are not aware.

An <b>INSSBuffer4</b> interface exists for every buffer object. To retrieve a pointer to an instance of <b>INSSBuffer4</b>, call the <b>QueryInterface</b> method of one of the other interfaces in the buffer object, typically <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>
</td>
<td>IID_INSSBuffer</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2">INSSBuffer2</a>
</td>
<td>IID_INSSBuffer2</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a>
</td>
<td>IID_INSSBuffer3</td>
</tr>
</table>

## -inheritance

The <b>INSSBuffer4</b> interface inherits from <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a>. <b>INSSBuffer4</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
