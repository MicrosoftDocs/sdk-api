---
UID: NF:certenc.ICertEncodeCRLDistInfo.SetNameCount
title: ICertEncodeCRLDistInfo::SetNameCount (certenc.h)
description: Sets a name count for the specified distribution point in a certificate revocation list (CRL) distribution information array.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","SetNameCount method","ICertEncodeCRLDistInfo interface [Security]","SetNameCount method","ICertEncodeCRLDistInfo.SetNameCount","ICertEncodeCRLDistInfo::SetNameCount","SetNameCount","SetNameCount method [Security]","SetNameCount method [Security]","CCertEncodeCRLDistInfo object","SetNameCount method [Security]","ICertEncodeCRLDistInfo interface","_certsrv_icertencodecrldistinfo_setnamecount","certenc/ICertEncodeCRLDistInfo::SetNameCount","security.icertencodecrldistinfo_setnamecount"]
old-location: security\icertencodecrldistinfo_setnamecount.htm
tech.root: security
ms.assetid: ce27adfd-e21a-4e8d-882e-72041f97958a
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],SetNameCount method, ICertEncodeCRLDistInfo interface [Security],SetNameCount method, ICertEncodeCRLDistInfo.SetNameCount, ICertEncodeCRLDistInfo::SetNameCount, SetNameCount, SetNameCount method [Security], SetNameCount method [Security],CCertEncodeCRLDistInfo object, SetNameCount method [Security],ICertEncodeCRLDistInfo interface, _certsrv_icertencodecrldistinfo_setnamecount, certenc/ICertEncodeCRLDistInfo::SetNameCount, security.icertencodecrldistinfo_setnamecount
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
 - ICertEncodeCRLDistInfo::SetNameCount
 - certenc/ICertEncodeCRLDistInfo::SetNameCount
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
 - ICertEncodeCRLDistInfo.SetNameCount
 - CCertEncodeCRLDistInfo.SetNameCount
---

# ICertEncodeCRLDistInfo::SetNameCount


## -description

The <b>SetNameCount</b> method sets a name count for the specified distribution point in a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information array.

## -parameters

### -param DistPointIndex [in]

Specifies the index of the distribution point for which to set the name count.

### -param NameCount [in]

Specifies the name count.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getnamecount">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnameentry">ICertEncodeCRLDistInfo::SetNameEntry</a>