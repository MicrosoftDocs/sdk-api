---
UID: NN:d3d9.IDirect3DCryptoSession9
title: IDirect3DCryptoSession9 (d3d9.h)
description: Represents a cryptographic session.To get a pointer to this interface, call IDirect3DDevice9Video::CreateCryptoSession.
old-location: mf\idirect3dcryptosession9.htm
tech.root: medfound
ms.assetid: 2511c9da-e696-4e49-b180-7fc1317c1652
ms.date: 12/05/2018
ms.keywords: IDirect3DCryptoSession9, IDirect3DCryptoSession9 interface [Media Foundation], IDirect3DCryptoSession9 interface [Media Foundation],described, d3d9/IDirect3DCryptoSession9, mf.idirect3dcryptosession9
f1_keywords:
- d3d9/IDirect3DCryptoSession9
dev_langs:
- c++
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- d3d9.h
api_name:
- IDirect3DCryptoSession9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DCryptoSession9 interface


## -description


Represents a cryptographic session.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession">IDirect3DDevice9Video::CreateCryptoSession</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DCryptoSession9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DCryptoSession9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DCryptoSession9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-encryptionblt"> EncryptionBlt</a>
</td>
<td align="left" width="63%">
Reads encrypted data from a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate"> GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-decryptionblt">DecryptionBlt</a>
</td>
<td align="left" width="63%">
Writes encrypted data to a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-finishsessionkeyrefresh">FinishSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Switches to a new session key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getencryptionbltkey">GetEncryptionBltKey</a>
</td>
<td align="left" width="63%">
Gets the key that is used to decrypt the data returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-encryptionblt">EncryptionBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getsurfacepitch">GetSurfacePitch</a>
</td>
<td align="left" width="63%">
Gets the stride of a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-negotiatekeyexchange">NegotiateKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes the session key for the cryptographic session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-startsessionkeyrefresh">StartSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Gets a random number that can be used to refresh the session key.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-interfaces">Direct3D Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>
 

 

