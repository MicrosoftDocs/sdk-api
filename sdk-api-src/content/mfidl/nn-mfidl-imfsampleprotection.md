---
UID: NN:mfidl.IMFSampleProtection
title: IMFSampleProtection (mfidl.h)
description: Provides encryption for media data inside the protected media path (PMP).
old-location: mf\imfsampleprotection.htm
tech.root: medfound
ms.assetid: bebe24cd-657b-4c6c-9fe9-5d6dd58827a3
ms.date: 12/05/2018
ms.keywords: IMFSampleProtection, IMFSampleProtection interface [Media Foundation], IMFSampleProtection interface [Media Foundation],described, bebe24cd-657b-4c6c-9fe9-5d6dd58827a3, mf.imfsampleprotection, mfidl/IMFSampleProtection
f1_keywords:
- mfidl/IMFSampleProtection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFSampleProtection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSampleProtection interface


## -description


Provides encryption for media data inside the protected media path (PMP).
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleProtection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSampleProtection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleProtection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsampleprotection-getinputprotectionversion">GetInputProtectionVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of sample protection that the component implements on input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsampleprotection-getoutputprotectionversion">GetOutputProtectionVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of sample protection that the component implements on output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsampleprotection-getprotectioncertificate">GetProtectionCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the sample protection certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsampleprotection-initinputprotection">InitInputProtection</a>
</td>
<td align="left" width="63%">
Initializes sample protection on the downstream component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsampleprotection-initoutputprotection">InitOutputProtection</a>
</td>
<td align="left" width="63%">
Retrieves initialization information for sample protection from the upstream component.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

