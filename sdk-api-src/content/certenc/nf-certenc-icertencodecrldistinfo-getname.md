---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetName
title: ICertEncodeCRLDistInfo::GetName (certenc.h)
description: Returns the name at a specified index of a certificate revocation list (CRL) distribution information point.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","GetName method","GetName","GetName method [Security]","GetName method [Security]","CCertEncodeCRLDistInfo object","GetName method [Security]","ICertEncodeCRLDistInfo interface","ICertEncodeCRLDistInfo interface [Security]","GetName method","ICertEncodeCRLDistInfo.GetName","ICertEncodeCRLDistInfo::GetName","_certsrv_icertencodecrldistinfo_getname","certenc/ICertEncodeCRLDistInfo::GetName","security.icertencodecrldistinfo_getname"]
old-location: security\icertencodecrldistinfo_getname.htm
tech.root: security
ms.assetid: a564af61-fb5e-46b7-a818-333b4d5e2f25
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CCertEncodeCRLDistInfo object, GetName method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetName method, ICertEncodeCRLDistInfo.GetName, ICertEncodeCRLDistInfo::GetName, _certsrv_icertencodecrldistinfo_getname, certenc/ICertEncodeCRLDistInfo::GetName, security.icertencodecrldistinfo_getname
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
 - ICertEncodeCRLDistInfo::GetName
 - certenc/ICertEncodeCRLDistInfo::GetName
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
 - ICertEncodeCRLDistInfo.GetName
 - CCertEncodeCRLDistInfo.GetName
---

# ICertEncodeCRLDistInfo::GetName


## -description

The <b>GetName</b> method returns the name at a specified index of a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information point.

## -parameters

### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get a name. The first value is at index zero.

### -param NameIndex [in]

Specifies the index of the name entry to get. The first value is at index zero.

### -param pstrName [out]

A pointer to a <b>BSTR</b> that represents the name value. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the name at the specified index of the specified distribution point. The return value is a <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getnamecount">ICertEncodeCRLDistInfo::GetNameCount</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnameentry">ICertEncodeCRLDistInfo::SetNameEntry</a>