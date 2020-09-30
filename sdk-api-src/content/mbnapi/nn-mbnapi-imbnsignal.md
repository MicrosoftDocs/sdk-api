---
UID: NN:mbnapi.IMbnSignal
title: IMbnSignal (mbnapi.h)
description: Get radio signal quality of a Mobile Broadband connection.
helpviewer_keywords: ["IMbnSignal","IMbnSignal interface [Microsoft Broadband Networks]","IMbnSignal interface [Microsoft Broadband Networks]","described","mbn.imbnsignal","mbnapi/IMbnSignal"]
old-location: mbn\imbnsignal.htm
tech.root: mbn
ms.assetid: 2b60d078-ccbd-4cc5-addf-e6e95832b3a1
ms.date: 12/05/2018
ms.keywords: IMbnSignal, IMbnSignal interface [Microsoft Broadband Networks], IMbnSignal interface [Microsoft Broadband Networks],described, mbn.imbnsignal, mbnapi/IMbnSignal
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnSignal
 - mbnapi/IMbnSignal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSignal
---

# IMbnSignal interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Get radio signal quality of a Mobile Broadband connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSignal</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnSignal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnSignal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignal-getsignalerror">GetSignalError</a>
</td>
<td align="left" width="63%">
Gets the received signal error rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignal-getsignalstrength">GetSignalStrength</a>
</td>
<td align="left" width="63%">
Gets the signal strength received by the device.

</td>
</tr>
</table>

## -remarks

The calling application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>