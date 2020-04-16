---
UID: NN:mfmediaengine.IMFMediaError
title: IMFMediaError (mfmediaengine.h)
description: Provides the current error status for the Media Engine.helpviewer_keywords: ["IMFMediaError","IMFMediaError interface [Media Foundation]","IMFMediaError interface [Media Foundation]","described","mf.imfmediaerror","mfmediaengine/IMFMediaError"]
old-location: mf\imfmediaerror.htm
tech.root: medfound
ms.assetid: 08F161FE-C0E5-44EE-923E-646ADA534C42
ms.date: 12/05/2018
ms.keywords: IMFMediaError, IMFMediaError interface [Media Foundation], IMFMediaError interface [Media Foundation],described, mf.imfmediaerror, mfmediaengine/IMFMediaError
f1_keywords:
- mfmediaengine/IMFMediaError
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- mfmediaengine.h
api_name:
- IMFMediaError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaError interface


## -description


Provides the current error status for the Media Engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaError</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaerror-geterrorcode">GetErrorCode</a>
</td>
<td align="left" width="63%">
Gets the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaerror-getextendederrorcode">GetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Gets the extended error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaerror-seterrorcode">SetErrorCode</a>
</td>
<td align="left" width="63%">
Sets the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaerror-setextendederrorcode">SetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Sets the extended error code.

</td>
</tr>
</table> 


## -remarks



The <b>IMFMediaError</b> interface corresponds to the <b>MediaError</b> object in HTML5.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-geterror">IMFMediaEngine::GetError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

