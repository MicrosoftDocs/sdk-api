---
UID: NF:certenroll.IX509PrivateKey.Create
title: IX509PrivateKey::Create (certenroll.h)
description: Creates an asymmetric private key.
helpviewer_keywords: ["Create","Create method [Security]","Create method [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","Create method","IX509PrivateKey.Create","IX509PrivateKey::Create","certenroll/IX509PrivateKey::Create","security.ix509privatekey_create_method"]
old-location: security\ix509privatekey_create_method.htm
tech.root: security
ms.assetid: e8c6564a-6009-437e-9b83-3711e43a7374
ms.date: 12/05/2018
ms.keywords: Create, Create method [Security], Create method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Create method, IX509PrivateKey.Create, IX509PrivateKey::Create, certenroll/IX509PrivateKey::Create, security.ix509privatekey_create_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PrivateKey::Create
 - certenroll/IX509PrivateKey::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Create
---

# IX509PrivateKey::Create


## -description

The <b>Create</b> method creates an asymmetric  <a href="/windows/desktop/SecGloss/p-gly">private key</a>.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

If you do not set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspstatus">CspStatus</a>, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a>, or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providertype">ProviderType</a> properties, this method uses the default provider, key size, and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a> values  when creating the key. On a new operating system installation, for example,  Microsoft Enhanced Cryptographic Provider v1.0 is the default provider.

If you do not set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a> property, this method automatically generates a name. The generated name includes a GUID and,  if the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containernameprefix">ContainerNamePrefix</a> property is not set, a prefix of "lp-". If the provider is a smart card provider, the generated name will not exceed the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_maxkeycontainernamelength">MaxKeyContainerNameLength</a> value specified by the provider. If the generated name initially exceeds this value, it is truncated to forty characters.

You cannot set the following properties after calling the <b>Create</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_algorithm">Algorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containernameprefix">ContainerNamePrefix</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspinformations">CspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspstatus">CspStatus</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_description">Description</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_existing">Existing</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_exportpolicy">ExportPolicy</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyprotection">KeyProtection</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyusage">KeyUsage</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_legacycsp">LegacyCsp</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_length">Length</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_machinecontext">MachineContext</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providertype">ProviderType</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-put_pin">Pin</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_readername">ReaderName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_silent">Silent</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
