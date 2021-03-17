---
UID: NF:certadm.IOCSPAdmin.GetHashAlgorithms
title: IOCSPAdmin::GetHashAlgorithms (certadm.h)
description: Gets a list of hash-algorithm names. The Online Certificate Status Protocol (OCSP) responder server uses these names to sign OCSP responses for a given certification authority (CA) configuration.
helpviewer_keywords: ["GetHashAlgorithms","GetHashAlgorithms method [Security]","GetHashAlgorithms method [Security]","IOCSPAdmin interface","IOCSPAdmin interface [Security]","GetHashAlgorithms method","IOCSPAdmin.GetHashAlgorithms","IOCSPAdmin::GetHashAlgorithms","certadm/IOCSPAdmin::GetHashAlgorithms","security.iocspadmin_gethashalgorithms"]
old-location: security\iocspadmin_gethashalgorithms.htm
tech.root: security
ms.assetid: aa131478-0456-4ae8-82a6-5dc8eaa293e0
ms.date: 12/05/2018
ms.keywords: GetHashAlgorithms, GetHashAlgorithms method [Security], GetHashAlgorithms method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetHashAlgorithms method, IOCSPAdmin.GetHashAlgorithms, IOCSPAdmin::GetHashAlgorithms, certadm/IOCSPAdmin::GetHashAlgorithms, security.iocspadmin_gethashalgorithms
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
 - IOCSPAdmin::GetHashAlgorithms
 - certadm/IOCSPAdmin::GetHashAlgorithms
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
 - IOCSPAdmin.GetHashAlgorithms
---

# IOCSPAdmin::GetHashAlgorithms


## -description

The <b>GetHashAlgorithms</b> method gets a list of hash-algorithm names. The Online Certificate Status Protocol (OCSP) responder server uses these names to sign OCSP responses for a given <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param bstrCAId [in]

A string that contains an <b>OCSPCAConfiguration</b> <a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_identifier">Identifier</a>.

### -param pVal [out]

The list of hash algorithms with which a responder server can sign responses.

## -returns

<h3>C++</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
A list of hash algorithms with which a responder server can sign responses.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>