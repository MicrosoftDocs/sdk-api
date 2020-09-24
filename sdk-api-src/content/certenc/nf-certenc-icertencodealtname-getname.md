---
UID: NF:certenc.ICertEncodeAltName.GetName
title: ICertEncodeAltName::GetName (certenc.h)
description: Returns the specified name from the alternate name array.
helpviewer_keywords: ["CCertEncodeAltName object [Security]","GetName method","GetName","GetName method [Security]","GetName method [Security]","CCertEncodeAltName object","GetName method [Security]","ICertEncodeAltName interface","ICertEncodeAltName interface [Security]","GetName method","ICertEncodeAltName.GetName","ICertEncodeAltName::GetName","_certsrv_icertencodealtname_getname","certenc/ICertEncodeAltName::GetName","security.icertencodealtname_getname"]
old-location: security\icertencodealtname_getname.htm
tech.root: security
ms.assetid: 25a3f36b-1c09-4b2e-84b7-a725d366fd77
ms.date: 12/05/2018
ms.keywords: CCertEncodeAltName object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CCertEncodeAltName object, GetName method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],GetName method, ICertEncodeAltName.GetName, ICertEncodeAltName::GetName, _certsrv_icertencodealtname_getname, certenc/ICertEncodeAltName::GetName, security.icertencodealtname_getname
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
 - ICertEncodeAltName::GetName
 - certenc/ICertEncodeAltName::GetName
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
 - ICertEncodeAltName.GetName
 - CCertEncodeAltName.GetName
---

# ICertEncodeAltName::GetName


## -description

The <b>GetName</b> method returns the specified name from the alternate name array.

## -parameters

### -param NameIndex [in]

A zero-based index that specifies the index of the alternate name entry to retrieve.  

To retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of a CERT_ALT_NAME_OTHER_NAME name, combine the index value with EAN_NAMEOBJECTID (defined as 0x80000000) with a bitwise-<b>OR</b> operation. Otherwise, the binary value is retrieved. To determine the type of name, call the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-getnamechoice">ICertEncodeAltName::GetNameChoice</a> method.

### -param pstrName [out]

A pointer to a <b>BSTR</b> that receives the alternate name. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the alternate name at the specified index. The return value is a <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodealtname">ICertEncodeAltName</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-getnamechoice">ICertEncodeAltName::GetNameChoice</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-setnameentry">ICertEncodeAltName::SetNameEntry</a>