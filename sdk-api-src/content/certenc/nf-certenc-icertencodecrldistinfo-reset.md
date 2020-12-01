---
UID: NF:certenc.ICertEncodeCRLDistInfo.Reset
title: ICertEncodeCRLDistInfo::Reset (certenc.h)
description: Resets a certificate revocation list (CRL) distribution information array to a specified number of distribution point structures.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","Reset method","ICertEncodeCRLDistInfo interface [Security]","Reset method","ICertEncodeCRLDistInfo.Reset","ICertEncodeCRLDistInfo::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertEncodeCRLDistInfo object","Reset method [Security]","ICertEncodeCRLDistInfo interface","_certsrv_icertencodecrldistinfo_reset","certenc/ICertEncodeCRLDistInfo::Reset","security.icertencodecrldistinfo_reset"]
old-location: security\icertencodecrldistinfo_reset.htm
tech.root: security
ms.assetid: 899de888-918f-4202-a324-0e603eba2324
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],Reset method, ICertEncodeCRLDistInfo interface [Security],Reset method, ICertEncodeCRLDistInfo.Reset, ICertEncodeCRLDistInfo::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeCRLDistInfo object, Reset method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_reset, certenc/ICertEncodeCRLDistInfo::Reset, security.icertencodecrldistinfo_reset
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeCRLDistInfo::Reset
 - certenc/ICertEncodeCRLDistInfo::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeCRLDistInfo.Reset
 - CCertEncodeCRLDistInfo.Reset
---

# ICertEncodeCRLDistInfo::Reset


## -description

The <b>Reset</b> method resets a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information array to a specified number of distribution point structures.

 The values of all the elements in the array of structures are set to zero.

## -parameters

### -param DistPointCount [in]

Specifies the number of CRL distribution points in the CRL distribution information array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getdistpointcount">ICertEncodeCRLDistInfo::GetDistPointCount</a>