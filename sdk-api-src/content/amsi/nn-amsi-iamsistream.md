---
UID: NN:amsi.IAmsiStream
title: IAmsiStream (amsi.h)
author: windows-sdk-content
description: Represents a stream to be scanned.
old-location: amsi\iamsistream.htm
tech.root: AMSI
ms.assetid: 409CE6BF-57A5-454E-91F9-3D66FE7E323F
ms.author: windowssdkdev
ms.date: 01/28/2019
ms.keywords: IAmsiStream, IAmsiStream interface [Antimalware Scan Interface], IAmsiStream interface [Antimalware Scan Interface],described, amsi.iamsistream, amsi/IAmsiStream
ms.topic: interface
f1_keywords: 
 - "amsi/IAmsiStream"
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amsi.h
api_name:
 - IAmsiStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAmsiStream interface

## -description

Represents a stream to be scanned. For a code example, see the [IAmsiStream interface sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAmsiStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAmsiStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAmsiStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-iamsistream-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Returns a requested attribute from the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-iamsistream-read">Read</a>
</td>
<td align="left" width="63%">
Requests a buffer-full of content to be read.

</td>
</tr>
</table> 
