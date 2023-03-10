---
UID: NF:xenroll.IEnroll4.createRequestWStr
title: IEnroll4::createRequestWStr (xenroll.h)
description: Creates a PKCS (IEnroll4.createRequestWStr)
helpviewer_keywords: ["IEnroll4 interface [Security]","createRequestWStr method","IEnroll4.createRequestWStr","IEnroll4::createRequestWStr","XECR_CMC","XECR_PKCS10_V1_5","XECR_PKCS10_V2_0","XECR_PKCS7","createRequestWStr","createRequestWStr method [Security]","createRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_createrequestwstr","xenroll/IEnroll4::createRequestWStr"]
old-location: security\ienroll4_createrequestwstr.htm
tech.root: security
ms.assetid: bc2b875c-96f8-453e-8f72-f9032d5aa773
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],createRequestWStr method, IEnroll4.createRequestWStr, IEnroll4::createRequestWStr, XECR_CMC, XECR_PKCS10_V1_5, XECR_PKCS10_V2_0, XECR_PKCS7, createRequestWStr, createRequestWStr method [Security], createRequestWStr method [Security],IEnroll4 interface, security.ienroll4_createrequestwstr, xenroll/IEnroll4::createRequestWStr
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
 - IEnroll4::createRequestWStr
 - xenroll/IEnroll4::createRequestWStr
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
 - IEnroll4.createRequestWStr
---

# IEnroll4::createRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createRequestWStr</b> method creates a PKCS #10, PKCS #7, or full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) format <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> and stores it in a BLOB. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

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

A pointer to a <b>null</b>-terminated Unicode string that contains the distinguished name (DN) of the entity for which the request is being made. The DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention, for example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an object identifier (OID) may be provided instead. This parameter may be <b>NULL</b>.

### -param pwszUsage [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the OID that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

### -param pblobRequest [out]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that receives the request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
