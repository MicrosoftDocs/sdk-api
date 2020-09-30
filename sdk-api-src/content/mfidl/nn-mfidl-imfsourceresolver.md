---
UID: NN:mfidl.IMFSourceResolver
title: IMFSourceResolver (mfidl.h)
description: Creates a media source from a URL or a byte stream.
helpviewer_keywords: ["079c61c5-7a29-4411-840e-9349190726ac","IMFSourceResolver","IMFSourceResolver interface [Media Foundation]","IMFSourceResolver interface [Media Foundation]","described","mf.imfsourceresolver","mfidl/IMFSourceResolver"]
old-location: mf\imfsourceresolver.htm
tech.root: mf
ms.assetid: 079c61c5-7a29-4411-840e-9349190726ac
ms.date: 12/05/2018
ms.keywords: 079c61c5-7a29-4411-840e-9349190726ac, IMFSourceResolver, IMFSourceResolver interface [Media Foundation], IMFSourceResolver interface [Media Foundation],described, mf.imfsourceresolver, mfidl/IMFSourceResolver
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceResolver
 - mfidl/IMFSourceResolver
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver
---

# IMFSourceResolver interface


## -description

Creates a media source from a URL or a byte stream. The <a href="/windows/desktop/medfound/source-resolver">Source Resolver</a> implements this interface. To create the source resolver, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver">MFCreateSourceResolver</a> function.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceResolver</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceResolver</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceResolver</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream">BeginCreateObjectFromByteStream</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create a media source from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl">BeginCreateObjectFromURL</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create a media source or a byte stream from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-cancelobjectcreation">CancelObjectCreation</a>
</td>
<td align="left" width="63%">
Cancels an asynchronous request to create an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream">CreateObjectFromByteStream</a>
</td>
<td align="left" width="63%">
Creates a media source from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl">CreateObjectFromURL</a>
</td>
<td align="left" width="63%">
Creates a media source or a byte stream from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream">EndCreateObjectFromByteStream</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create a media source from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl">EndCreateObjectFromURL</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create an object from a URL.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>