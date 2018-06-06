---
UID: NF:certenroll.ICertPropertyKeyProvInfo.Initialize
title: ICertPropertyKeyProvInfo::Initialize
author: windows-sdk-content
description: Initializes the object from a private key.
old-location: security\icertpropertykeyprovinfo_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: bc317b7b-c4d8-480b-9de7-3324e30898b8
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertPropertyKeyProvInfo interface [Security],Initialize method, ICertPropertyKeyProvInfo.Initialize, ICertPropertyKeyProvInfo::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyKeyProvInfo interface, certenroll/ICertPropertyKeyProvInfo::Initialize, security.icertpropertykeyprovinfo_initialize_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyKeyProvInfo.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyKeyProvInfo::Initialize


## -description


The <b>Initialize</b> method initializes the object from a private key.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface that represents the private key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> pointer is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_ARITHMETIC_OVERFLOW</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The unique container name and the provider name are too long.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/24cc6dea-fb29-4533-8f6c-3f273c5b94c3">PrivateKey</a> property to retrieve the key.

The <b>Initialize</b> method opens the private key and verifies that the following <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> properties are set:<ul>
<li>
<a href="https://msdn.microsoft.com/81cf4689-0cd6-4185-9242-ef26de9161a1">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93da413f-556d-4cda-8628-ce4a2150da19">UniqueContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bdc3278e-3b5a-4ad0-9e9b-9639a2db4040">MachineContext</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/1c35c2f0-8e79-4031-bae2-2be081f3c8dd">ICertPropertyKeyProvInfo</a>
 

 

