---
UID: NN:bits10_2.IBackgroundCopyJobHttpOptions2
title: IBackgroundCopyJobHttpOptions2 (bits10_2.h)
description: Use this interface to retrieve and/or to override the HTTP method used for a BITS transfer.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions2","IBackgroundCopyJobHttpOptions2 interface [BITS]","IBackgroundCopyJobHttpOptions2 interface [BITS]","described","bits.ibackgroundcopyjobhttpoptions2","bits10_2/IBackgroundCopyJobHttpOptions2"]
old-location: bits\ibackgroundcopyjobhttpoptions2.htm
tech.root: Bits
ms.assetid: 6E8A32CF-99F6-4C4D-A6EE-A05A1E601793
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJobHttpOptions2, IBackgroundCopyJobHttpOptions2 interface [BITS], IBackgroundCopyJobHttpOptions2 interface [BITS],described, bits.ibackgroundcopyjobhttpoptions2, bits10_2/IBackgroundCopyJobHttpOptions2
req.header: bits10_2.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions2
 - bits10_2/IBackgroundCopyJobHttpOptions2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions2
---

# IBackgroundCopyJobHttpOptions2 interface


## -description

Use this interface to retrieve and/or to override  the HTTP method used for a BITS transfer.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using __uuidof(IBackgroundCopyJobHttpOptions2) for the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJobHttpOptions2</b> interface inherits from <a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>. <b>IBackgroundCopyJobHttpOptions2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJobHttpOptions2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/bits10_2/nf-bits10_2-ibackgroundcopyjobhttpoptions2-gethttpmethod">GetHttpMethod</a>
</td>
<td align="left" width="63%">
Retrieves a wide string containing the HTTP method name for the BITS transfer. By default, download jobs will be "GET", and upload and upload-reply jobs will be "BITS_POST".

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/bits10_2/nf-bits10_2-ibackgroundcopyjobhttpoptions2-sethttpmethod">SetHttpMethod</a>
</td>
<td align="left" width="63%">
Overrides the default HTTP method used for a BITS transfer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>
