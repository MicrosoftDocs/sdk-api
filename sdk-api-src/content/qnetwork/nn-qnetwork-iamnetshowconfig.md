---
UID: NN:qnetwork.IAMNetShowConfig
title: IAMNetShowConfig (qnetwork.h)
description: The IAMNetShowConfig interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
helpviewer_keywords: ["IAMNetShowConfig","IAMNetShowConfig interface [DirectShow]","IAMNetShowConfig interface [DirectShow]","described","IAMNetShowConfigInterface","dshow.iamnetshowconfig","qnetwork/IAMNetShowConfig"]
old-location: dshow\iamnetshowconfig.htm
tech.root: dshow
ms.assetid: 611b43dc-7f6d-404e-90a4-b109b9475fb6
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig, IAMNetShowConfig interface [DirectShow], IAMNetShowConfig interface [DirectShow],described, IAMNetShowConfigInterface, dshow.iamnetshowconfig, qnetwork/IAMNetShowConfig
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowConfig
 - qnetwork/IAMNetShowConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowConfig
---

# IAMNetShowConfig interface


## -description

The <code>IAMNetShowConfig</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter implements this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowConfig</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMNetShowConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
