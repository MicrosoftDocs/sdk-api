---
UID: NN:vfw.IAVIEditStream
title: IAVIEditStream (vfw.h)
description: The IAVIEditStream interface supports manipulating and modifying editable streams. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
helpviewer_keywords: ["IAVIEditStream","IAVIEditStream interface [Windows Multimedia]","IAVIEditStream interface [Windows Multimedia]","described","_win32_IAVIEditStream","multimedia.iavieditstream","vfw/IAVIEditStream"]
old-location: multimedia\iavieditstream.htm
tech.root: Multimedia
ms.assetid: d32dc386-05cf-4f7b-9785-a38586a09402
ms.date: 12/05/2018
ms.keywords: IAVIEditStream, IAVIEditStream interface [Windows Multimedia], IAVIEditStream interface [Windows Multimedia],described, _win32_IAVIEditStream, multimedia.iavieditstream, vfw/IAVIEditStream
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAVIEditStream
 - vfw/IAVIEditStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIEditStream
---

# IAVIEditStream interface


## -description

The <b>IAVIEditStream</b> interface supports manipulating and modifying editable streams. Uses <a href="/previous-versions/dd757101(v=vs.85)">IUnknown::QueryInterface</a>, <a href="/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a>, <a href="/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> in addition to the following custom methods:

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIEditStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAVIEditStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIEditStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vfw/nf-vfw-iavieditstream-clone">Clone</a>
</td>
<td align="left" width="63%">
Duplicates a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vfw/nf-vfw-iavieditstream-copy">Copy</a>
</td>
<td align="left" width="63%">
Copies a stream or a portion of it to a temporary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vfw/nf-vfw-iavieditstream-cut">Cut</a>
</td>
<td align="left" width="63%">
Removes a portion of a stream and places it in a temporary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vfw/nf-vfw-iavieditstream-paste">Paste</a>
</td>
<td align="left" width="63%">
Copies a stream or a portion of it and places it in another stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vfw/nf-vfw-iavieditstream-setinfo">SetInfo</a>
</td>
<td align="left" width="63%">
Changes the characteristics of a stream.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>