---
UID: NN:qnetwork.IAMNetworkStatus
title: IAMNetworkStatus (qnetwork.h)
description: The IAMNetworkStatus interface reports the quality of the network connection for the legacy Windows Media Player 6.4 source filter.
helpviewer_keywords: ["IAMNetworkStatus","IAMNetworkStatus interface [DirectShow]","IAMNetworkStatus interface [DirectShow]","described","IAMNetworkStatusInterface","dshow.iamnetworkstatus","qnetwork/IAMNetworkStatus"]
old-location: dshow\iamnetworkstatus.htm
tech.root: dshow
ms.assetid: 51d56b76-f9fc-44e1-88f0-d35d861a4697
ms.date: 12/05/2018
ms.keywords: IAMNetworkStatus, IAMNetworkStatus interface [DirectShow], IAMNetworkStatus interface [DirectShow],described, IAMNetworkStatusInterface, dshow.iamnetworkstatus, qnetwork/IAMNetworkStatus
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
 - IAMNetworkStatus
 - qnetwork/IAMNetworkStatus
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
 - IAMNetworkStatus
---

# IAMNetworkStatus interface


## -description

The <code>IAMNetworkStatus</code> interface reports the quality of the network connection for the legacy Windows Media Player 6.4 source filter. The <a href="/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter implements this interface. It enables clients to retrieve information about the quality of the network connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetworkStatus</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMNetworkStatus</b> also has these types of members:
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
