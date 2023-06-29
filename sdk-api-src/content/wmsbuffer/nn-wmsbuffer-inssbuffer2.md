---
UID: NN:wmsbuffer.INSSBuffer2
title: INSSBuffer2 (wmsbuffer.h)
description: The INSSBuffer2 interface inherits from INSSBuffer and defines two additional methods. Currently, neither of these methods is implemented.
helpviewer_keywords: ["INSSBuffer2","INSSBuffer2 interface [windows Media Format]","INSSBuffer2 interface [windows Media Format]","described","INSSBuffer2Interface","wmformat.inssbuffer2","wmsbuffer/INSSBuffer2"]
old-location: wmformat\inssbuffer2.htm
tech.root: wmformat
ms.assetid: 74d174a1-ede8-482c-ae42-19ca65c6cad4
ms.date: 4/26/2023
ms.keywords: INSSBuffer2, INSSBuffer2 interface [windows Media Format], INSSBuffer2 interface [windows Media Format],described, INSSBuffer2Interface, wmformat.inssbuffer2, wmsbuffer/INSSBuffer2
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
 - INSSBuffer2
 - wmsbuffer/INSSBuffer2
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
 - INSSBuffer2
 - INSSBuffer2.GetSampleProperties
 - INSSBuffer2.SetSampleProperties
---

# INSSBuffer2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>INSSBuffer2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> and defines two additional methods. Currently, neither of these methods is implemented.



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
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a>
</td>
<td>IID_INSSBuffer3</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4">INSSBuffer4</a>
</td>
<td>IID_INSSBuffer4</td>
</tr>
</table>

## -inheritance

The <b>INSSBuffer2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>. <b>INSSBuffer2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
