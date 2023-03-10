---
UID: NF:xenroll.IEnroll4.createFileRequestWStr
title: IEnroll4::createFileRequestWStr (xenroll.h)
description: Creates a PKCS (IEnroll4.createFileRequestWStr)
helpviewer_keywords: ["IEnroll4 interface [Security]","createFileRequestWStr method","IEnroll4.createFileRequestWStr","IEnroll4::createFileRequestWStr","XECR_CMC","XECR_PKCS10_V1_5","XECR_PKCS10_V2_0","XECR_PKCS7","createFileRequestWStr","createFileRequestWStr method [Security]","createFileRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_createfilerequestwstr","xenroll/IEnroll4::createFileRequestWStr"]
old-location: security\ienroll4_createfilerequestwstr.htm
tech.root: security
ms.assetid: 5750f2ad-a96f-4bc7-9a1f-354e279a7860
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],createFileRequestWStr method, IEnroll4.createFileRequestWStr, IEnroll4::createFileRequestWStr, XECR_CMC, XECR_PKCS10_V1_5, XECR_PKCS10_V2_0, XECR_PKCS7, createFileRequestWStr, createFileRequestWStr method [Security], createFileRequestWStr method [Security],IEnroll4 interface, security.ienroll4_createfilerequestwstr, xenroll/IEnroll4::createFileRequestWStr
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll4::createFileRequestWStr
 - xenroll/IEnroll4::createFileRequestWStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.createFileRequestWStr
---

# IEnroll4::createFileRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFileRequestWStr</b> method creates a PKCS #10, PKCS #7, or full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) format <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> and stores it in a file. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param Flags [in]

Value specifying the type of certificate request to create. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XECR_CMC"></a><a id="xecr_cmc"></a><dl>
<dt><b>XECR_CMC</b></dt>
</dl>
</td>
<td width="60%">
Full CMC

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V1_5"></a><a id="xecr_pkcs10_v1_5"></a><dl>
<dt><b>XECR_PKCS10_V1_5</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V2_0"></a><a id="xecr_pkcs10_v2_0"></a><dl>
<dt><b>XECR_PKCS10_V2_0</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10 version 2

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS7"></a><a id="xecr_pkcs7"></a><dl>
<dt><b>XECR_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
PKCS #7

</td>
</tr>
</table>

### -param pwszDNName [in]

A pointer to a <b>null</b>-terminated wide character string that represents the distinguished name (DN) of the entity for which the request is being made. The DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention, for example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an object identifier (OID) may be provided instead. This parameter may be <b>NULL</b>.

### -param pwszUsage [in]

A pointer to a <b>null</b>-terminated wide character string for the OID that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

### -param pwszRequestFileName [in]

A pointer to a <b>null</b>-terminated wide character string that contains the name of the file that will receive the request.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
