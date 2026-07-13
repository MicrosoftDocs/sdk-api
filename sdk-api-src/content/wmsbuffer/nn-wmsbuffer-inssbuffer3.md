---
UID: NN:wmsbuffer.INSSBuffer3
title: INSSBuffer3 (wmsbuffer.h)
description: The INSSBuffer3 interface enhances the INSSBuffer interface by adding the ability to set and retrieve single properties for a sample.
helpviewer_keywords: ["INSSBuffer3","INSSBuffer3 interface [windows Media Format]","INSSBuffer3 interface [windows Media Format]","described","INSSBuffer3Interface","wmformat.inssbuffer3","wmsbuffer/INSSBuffer3"]
old-location: wmformat\inssbuffer3.htm
tech.root: wmformat
ms.assetid: 3ebf80d0-b5b0-4024-805d-e0a3855574bf
ms.date: 4/26/2023
ms.keywords: INSSBuffer3, INSSBuffer3 interface [windows Media Format], INSSBuffer3 interface [windows Media Format],described, INSSBuffer3Interface, wmformat.inssbuffer3, wmsbuffer/INSSBuffer3
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
 - INSSBuffer3
 - wmsbuffer/INSSBuffer3
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
 - INSSBuffer3
---

# INSSBuffer3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>INSSBuffer3</b> interface enhances the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface by adding the ability to set and retrieve single properties for a sample. This interface inherits its functionality from the <b>INSSBuffer2</b> interface, which inherits functionality from <b>INSSBuffer</b>. <b>INSSBuffer2</b> is not documented separately in this documentation because the two methods it exposes are not implemented at this time.

To obtain a pointer to the <b>INSSBuffer3</b> interface of an existing buffer object, call <b>INSSBuffer::QueryInterface</b>.



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
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4">INSSBuffer4</a>
</td>
<td>IID_INSSBuffer4</td>
</tr>
</table>

## -inheritance

The <b>INSSBuffer3</b> interface inherits from <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>. <b>INSSBuffer3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
