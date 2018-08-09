---
UID: NN:d3d9.IDirect3DCryptoSession9
title: IDirect3DCryptoSession9
author: windows-sdk-content
description: Represents a cryptographic session.To get a pointer to this interface, call IDirect3DDevice9Video::CreateCryptoSession.
old-location: mf\idirect3dcryptosession9.htm
old-project: medfound
ms.assetid: 2511c9da-e696-4e49-b180-7fc1317c1652
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IDirect3DCryptoSession9, IDirect3DCryptoSession9 interface [Media Foundation], IDirect3DCryptoSession9 interface [Media Foundation],described, d3d9/IDirect3DCryptoSession9, mf.idirect3dcryptosession9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DCryptoSession9 interface


## -description


Represents a cryptographic session.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/1c0e3aa4-94d5-4398-a6c0-5466a437162d">IDirect3DDevice9Video::CreateCryptoSession</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DCryptoSession9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DCryptoSession9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/42aa21d3-7c38-4058-b766-454be8b1ae80"> EncryptionBlt</a>
</td>
<td align="left" width="63%">
Reads encrypted data from a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/802285a6-1338-4131-bb5e-9d4daad62bdc"> GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03032a3f-e10f-4f40-837e-01b7b113b29e">DecryptionBlt</a>
</td>
<td align="left" width="63%">
Writes encrypted data to a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451648">FinishSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Switches to a new session key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451654">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451660">GetEncryptionBltKey</a>
</td>
<td align="left" width="63%">
Gets the key that is used to decrypt the data returned by the <a href="https://msdn.microsoft.com/42aa21d3-7c38-4058-b766-454be8b1ae80">EncryptionBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f9f637e-a693-4fc5-9bf9-a6900aa2ed8c">GetSurfacePitch</a>
</td>
<td align="left" width="63%">
Gets the stride of a protected surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e12f169-b121-400d-9244-8d7d0097c030">NegotiateKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes the session key for the cryptographic session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451696">StartSessionKeyRefresh</a>
</td>
<td align="left" width="63%">
Gets a random number that can be used to refresh the session key.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>
 

 

