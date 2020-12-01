---
UID: NF:certadm.IOCSPAdmin.GetSigningCertificates
title: IOCSPAdmin::GetSigningCertificates (certadm.h)
description: Gets the signing certificates that are available on a responder server for a given certification authority (CA) certificate.
helpviewer_keywords: ["GetSigningCertificates","GetSigningCertificates method [Security]","GetSigningCertificates method [Security]","IOCSPAdmin interface","IOCSPAdmin interface [Security]","GetSigningCertificates method","IOCSPAdmin.GetSigningCertificates","IOCSPAdmin::GetSigningCertificates","certadm/IOCSPAdmin::GetSigningCertificates","security.iocspadmin_getsigningcertificates"]
old-location: security\iocspadmin_getsigningcertificates.htm
tech.root: security
ms.assetid: 762dc32f-90d4-4e88-a3cc-e77e729f0a98
ms.date: 12/05/2018
ms.keywords: GetSigningCertificates, GetSigningCertificates method [Security], GetSigningCertificates method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetSigningCertificates method, IOCSPAdmin.GetSigningCertificates, IOCSPAdmin::GetSigningCertificates, certadm/IOCSPAdmin::GetSigningCertificates, security.iocspadmin_getsigningcertificates
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::GetSigningCertificates
 - certadm/IOCSPAdmin::GetSigningCertificates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.GetSigningCertificates
---

# IOCSPAdmin::GetSigningCertificates


## -description

The <b>GetSigningCertificates</b> method  gets the signing certificates that are available on a responder server for a given <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate. This method only returns signing certificates from the <b>CERT_SYSTEM_STORE_LOCAL_MACHINE</b> system store for the specified server.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param pCACertVar [in]

The CA certificate for which to retrieve signing certificates.

### -param pVal [out]

## -returns

<h3>C++</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The available signing certificates.

## -remarks

Each signing certificate has the following properties:

<ul>
<li>Signed by the CA specified by the <i>pCACertVar</i> parameter</li>
<li>Includes the Online Certificate Status Protocol (OCSP) signing (<b>XCN_OID_PKIX_KP_OCSP_SIGNING</b>) extension</li>
<li>Has not expired</li>
<li>Responder server can access the certificate private key</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>