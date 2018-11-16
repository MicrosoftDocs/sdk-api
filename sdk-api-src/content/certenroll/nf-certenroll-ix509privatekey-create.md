---
UID: NF:certenroll.IX509PrivateKey.Create
title: IX509PrivateKey::Create
author: windows-sdk-content
description: Creates an asymmetric private key.
old-location: security\ix509privatekey_create_method.htm
tech.root: SecCertEnroll
ms.assetid: e8c6564a-6009-437e-9b83-3711e43a7374
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Create, Create method [Security], Create method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Create method, IX509PrivateKey.Create, IX509PrivateKey::Create, certenroll/IX509PrivateKey::Create, security.ix509privatekey_create_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509PrivateKey.Create
: 
---

# IX509PrivateKey::Create


## -description


The <b>Create</b> method creates an asymmetric  <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BUSY)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The CSP handle is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key already exists.

</td>
</tr>
</table>
 




## -remarks



If you do not set the <a href="https://msdn.microsoft.com/en-us/library/Aa378972(v=VS.85).aspx">CspStatus</a>, the <a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a>, or <a href="https://msdn.microsoft.com/en-us/library/Aa379032(v=VS.85).aspx">ProviderType</a> properties, this method uses the default provider, key size, and <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> values  when creating the key. On a new operating system installation, for example,  Microsoft Enhanced Cryptographic Provider v1.0 is the default provider.

If you do not set the <a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a> property, this method automatically generates a name. The generated name includes a GUID and,  if the <a href="https://msdn.microsoft.com/en-us/library/Aa378946(v=VS.85).aspx">ContainerNamePrefix</a> property is not set, a prefix of "lp-". If the provider is a smart card provider, the generated name will not exceed the <a href="https://msdn.microsoft.com/en-us/library/Aa376753(v=VS.85).aspx">MaxKeyContainerNameLength</a> value specified by the provider. If the generated name initially exceeds this value, it is truncated to forty characters.

You cannot set the following properties after calling the <b>Create</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa379027(v=VS.85).aspx">Open</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378926(v=VS.85).aspx">Algorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378946(v=VS.85).aspx">ContainerNamePrefix</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378966(v=VS.85).aspx">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378972(v=VS.85).aspx">CspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa965843(v=VS.85).aspx">Description</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378993(v=VS.85).aspx">Existing</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379002(v=VS.85).aspx">ExportPolicy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa965844(v=VS.85).aspx">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379019(v=VS.85).aspx">KeyProtection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379021(v=VS.85).aspx">KeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379023(v=VS.85).aspx">Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379024(v=VS.85).aspx">MachineContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379032(v=VS.85).aspx">ProviderType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379029(v=VS.85).aspx">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379033(v=VS.85).aspx">ReaderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379035(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379036(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

