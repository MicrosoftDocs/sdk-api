---
UID: NF:certenroll.IX509PrivateKey.Open
title: IX509PrivateKey::Open (certenroll.h)
description: Opens an existing private key.
helpviewer_keywords: ["IX509PrivateKey interface [Security]","Open method","IX509PrivateKey.Open","IX509PrivateKey::Open","Open","Open method [Security]","Open method [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::Open","security.ix509privatekey_open_method"]
old-location: security\ix509privatekey_open_method.htm
tech.root: security
ms.assetid: 965e3bf8-22b9-4015-8fb2-102c5f7b1cb5
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],Open method, IX509PrivateKey.Open, IX509PrivateKey::Open, Open, Open method [Security], Open method [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Open, security.ix509privatekey_open_method
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
 - IX509PrivateKey::Open
 - certenroll/IX509PrivateKey::Open
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
 - IX509PrivateKey.Open
---

# IX509PrivateKey::Open


## -description

The <b>Open</b> method opens an existing <a href="/windows/desktop/SecGloss/p-gly">private key</a>.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If successful, this method sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_opened">Opened</a> property. You must call either the <b>Open</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> methods before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-export">Export</a> method or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-exportpublickey">ExportPublicKey</a> method.

You cannot set the following properties after calling the <b>Open</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
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


The following properties can be set regardless of whether the key is open:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_certificate">Certificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_securitydescriptor">SecurityDescriptor</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
