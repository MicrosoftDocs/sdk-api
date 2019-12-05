---
UID: NN:mfidl.IMFContentDecryptorContext
title: IMFContentDecryptorContext (mfidl.h)
description: Allows a decryptor to manage hardware keys and decrypt hardware samples.
old-location: mf\imfcontentdecryptorcontext.htm
tech.root: medfound
ms.assetid: 94DB835F-3D2A-4CC8-A1CF-10215E3D30D6
ms.date: 12/05/2018
ms.keywords: IMFContentDecryptorContext, IMFContentDecryptorContext interface [Media Foundation], IMFContentDecryptorContext interface [Media Foundation],described, mf.imfcontentdecryptorcontext, mfidl/IMFContentDecryptorContext
ms.topic: interface
f1_keywords:
- mfidl/IMFContentDecryptorContext
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.dll
api_name:
- IMFContentDecryptorContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFContentDecryptorContext interface


## -description


Allows a decryptor to manage hardware keys and decrypt hardware samples.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentDecryptorContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFContentDecryptorContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFContentDecryptorContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentdecryptorcontext-initializehardwarekey">InitializeHardwareKey</a>
</td>
<td align="left" width="63%">
 Allows the display driver to return IHV-specific information used when initializing a new hardware key. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

