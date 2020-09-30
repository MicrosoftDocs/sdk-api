---
UID: NN:strmif.IAMovieSetup
title: IAMovieSetup (strmif.h)
description: Note  This interface has been deprecated.
helpviewer_keywords: ["IAMovieSetup","IAMovieSetup interface [DirectShow]","IAMovieSetup interface [DirectShow]","described","IAMovieSetupInterface","dshow.iamoviesetup","strmif/IAMovieSetup"]
old-location: dshow\iamoviesetup.htm
tech.root: dshow
ms.assetid: b200dbee-bab7-43d7-a204-751592fa2405
ms.date: 12/05/2018
ms.keywords: IAMovieSetup, IAMovieSetup interface [DirectShow], IAMovieSetup interface [DirectShow],described, IAMovieSetupInterface, dshow.iamoviesetup, strmif/IAMovieSetup
req.header: strmif.h
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
 - IAMovieSetup
 - strmif/IAMovieSetup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMovieSetup
---

# IAMovieSetup interface


## -description

<div class="alert"><b>Note</b>  This interface has been deprecated. It is used by two obsolete functions, <a href="/windows/desktop/DirectShow/amoviedllregisterserver">AMovieDllRegisterServer</a> and <a href="/windows/desktop/DirectShow/amoviedllunregisterserver">AMovieDllUnregisterServer</a>. These functions are now replaced by <a href="/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a>, which does not require <b>IAMovieSetup</b>. However, <b>IAMovieSetup</b> will continue to be supported for backward compatibility with existing applications.</div>
<div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMovieSetup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMovieSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMovieSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamoviesetup-register">Register</a>
</td>
<td align="left" width="63%">
Adds the filter to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamoviesetup-unregister">Unregister</a>
</td>
<td align="left" width="63%">
Removes the filter from the registry.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>