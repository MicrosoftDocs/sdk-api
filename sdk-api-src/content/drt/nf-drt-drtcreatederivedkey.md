---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DrtCreateDerivedKey function


## -description


The <b>DrtCreateDerivedKey</b> function creates a key that can be utilized by <a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a> when the DRT is using a derived key security provider.


## -parameters




### -param pLocalCert [in]

Pointer to the certificate that is the "local" portion of the chain.  The root of this chain must match the root specified by <i>pRootCert</i> in <a href="https://msdn.microsoft.com/e4cc8326-e2bc-459f-97dd-a00cfd1ed35e">DrtCreateDerivedKeySecurityProvider</a>. This certificate is used to generate a key that is used to register and prove "key ownership" with the DRT.


### -param pKey [out]

Pointer to the created key.


#### - pRootCert [in]

Pointer to the certificate that is the "root" portion of the chain. The local cert must be signed by a chain of certificates including the root cert.  This root cert will be used to verify certificates presented by other members of the mesh.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li><i>pLocalCert</i> is <b>NULL</b>.</li>
<li><i>pKey</i> is <b>NULL</b>.</li>
<li>The <b>pb</b> member in the <a href="https://msdn.microsoft.com/ee81daca-e889-471e-b43b-4593380a55dd">DRT_DATA</a> structure  is <b>NULL</b>.</li>
<li>The <b>cb</b> member in the <a href="https://msdn.microsoft.com/ee81daca-e889-471e-b43b-4593380a55dd">DRT_DATA</a> structure is not equal to 32 bytes.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_CAPABILITY_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>The requested security algorithms are not available ( ie. BCRYPT_SHA256_ALGORITHM or  BCRYPT_AES_ALGORITHM).</li>
<li>The <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> operation failed.</li>
<li>The <i>dwProvType</i> parameter  indicates that the certificate provider is not AES capable.</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e4cc8326-e2bc-459f-97dd-a00cfd1ed35e">DrtCreateDerivedKeySecurityProvider</a>



<a href="https://msdn.microsoft.com/89b2bbe6-51a3-48fc-85c9-13e1b0cfd880">DrtDeleteDerivedKeySecurityProvider</a>



<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>
 

 

