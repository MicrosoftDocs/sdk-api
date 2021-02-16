---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetNameCount
title: ICertEncodeCRLDistInfo::GetNameCount (certenc.h)
description: Returns the number of names in a certificate revocation list (CRL) distribution point.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","GetNameCount method","GetNameCount","GetNameCount method [Security]","GetNameCount method [Security]","CCertEncodeCRLDistInfo object","GetNameCount method [Security]","ICertEncodeCRLDistInfo interface","ICertEncodeCRLDistInfo interface [Security]","GetNameCount method","ICertEncodeCRLDistInfo.GetNameCount","ICertEncodeCRLDistInfo::GetNameCount","_certsrv_icertencodecrldistinfo_getnamecount","certenc/ICertEncodeCRLDistInfo::GetNameCount","security.icertencodecrldistinfo_getnamecount"]
old-location: security\icertencodecrldistinfo_getnamecount.htm
tech.root: security
ms.assetid: 64102b89-defe-4f26-b6b2-8c3903e08347
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetNameCount method, GetNameCount, GetNameCount method [Security], GetNameCount method [Security],CCertEncodeCRLDistInfo object, GetNameCount method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetNameCount method, ICertEncodeCRLDistInfo.GetNameCount, ICertEncodeCRLDistInfo::GetNameCount, _certsrv_icertencodecrldistinfo_getnamecount, certenc/ICertEncodeCRLDistInfo::GetNameCount, security.icertencodecrldistinfo_getnamecount
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
 - ICertEncodeCRLDistInfo::GetNameCount
 - certenc/ICertEncodeCRLDistInfo::GetNameCount
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
 - ICertEncodeCRLDistInfo.GetNameCount
 - CCertEncodeCRLDistInfo.GetNameCount
---

# ICertEncodeCRLDistInfo::GetNameCount


## -description

The <b>GetNameCount</b> method returns the number of names in a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution point.

## -parameters

### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get the name count.

### -param pNameCount [out]

A pointer to a <b>Long</b> that will represent the number of name values contained in the CRL distribution point.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of names in the CRL distribution point.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getdistpointcount">ICertEncodeCRLDistInfo::GetDistPointCount</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getname">ICertEncodeCRLDistInfo::GetName</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnamecount">ICertEncodeCRLDistInfo::SetNameCount</a>