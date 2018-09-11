---
UID: NF:drt.DrtCreateDerivedKeySecurityProvider
title: DrtCreateDerivedKeySecurityProvider function
author: windows-sdk-content
description: DrtCreateDerivedKeySecurityProvider function creates the derived key security provider for a Distributed Routing Table.
old-location: p2p\drtcreatederivedkeysecurityprovider.htm
tech.root: p2psdk
ms.assetid: e4cc8326-e2bc-459f-97dd-a00cfd1ed35e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrtCreateDerivedKeySecurityProvider, DrtCreateDerivedKeySecurityProvider function [Peer Networking], drt/DrtCreateDerivedKeySecurityProvider, p2p.drtcreatederivedkeysecurityprovider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateDerivedKeySecurityProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtCreateDerivedKeySecurityProvider function


## -description


The <b>DrtCreateDerivedKeySecurityProvider</b> function creates the derived key security provider for a Distributed Routing Table.


## -parameters




### -param pRootCert [in]

Pointer to the certificate that is the "root" portion of the chain. This is used to ensure that keys derived from the same chain can be verified.


### -param pLocalCert [out]

Pointer to the <a href="https://msdn.microsoft.com/1eedfff3-d561-462e-bad0-45e7bc46fb1a">DRT_SECURITY_PROVIDER</a> module to be included in the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


### -param ppSecurityProvider

TBD




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
<i>pRootCert</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system could not allocate memory for the security provider.

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
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_CERT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
No certificate store attached or there is an error in the certificate chain.

</td>
</tr>
</table>
 




## -remarks



The security provider created by this function is specific to the DRT it was created for. It cannot be shared by multiple DRT instances.




## -see-also




<a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a>



<a href="https://msdn.microsoft.com/069358e0-4b61-44ed-b235-37f1d038feff">DrtCreateDerivedKey</a>



<a href="https://msdn.microsoft.com/89b2bbe6-51a3-48fc-85c9-13e1b0cfd880">DrtDeleteDerivedKeySecurityProvider</a>
 

 

