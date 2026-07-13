---
UID: NF:xenroll.ICEnroll4.createFileRequest
title: ICEnroll4::createFileRequest (xenroll.h)
description: Creates a PKCS (ICEnroll4.createFileRequest)
helpviewer_keywords: ["CEnroll object [Security]","createFileRequest method","ICEnroll4 interface [Security]","createFileRequest method","ICEnroll4.createFileRequest","ICEnroll4::createFileRequest","XECR_CMC","XECR_PKCS10_V1_5","XECR_PKCS10_V2_0","XECR_PKCS7","_xen_icenroll4_createfilerequest","createFileRequest","createFileRequest method [Security]","createFileRequest method [Security]","CEnroll object","createFileRequest method [Security]","ICEnroll4 interface","security.icenroll4_createfilerequest","xenroll/ICEnroll4::createFileRequest"]
old-location: security\icenroll4_createfilerequest.htm
tech.root: security
ms.assetid: 8902eb8e-c597-42a6-8836-6a24181da4d4
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createFileRequest method, ICEnroll4 interface [Security],createFileRequest method, ICEnroll4.createFileRequest, ICEnroll4::createFileRequest, XECR_CMC, XECR_PKCS10_V1_5, XECR_PKCS10_V2_0, XECR_PKCS7, _xen_icenroll4_createfilerequest, createFileRequest, createFileRequest method [Security], createFileRequest method [Security],CEnroll object, createFileRequest method [Security],ICEnroll4 interface, security.icenroll4_createfilerequest, xenroll/ICEnroll4::createFileRequest
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
 - ICEnroll4::createFileRequest
 - xenroll/ICEnroll4::createFileRequest
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
 - ICEnroll4.createFileRequest
 - CEnroll.createFileRequest
---

# ICEnroll4::createFileRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFileRequest</b> method creates a PKCS #10 certificate request, a PKCS #7 request, or a full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) request and stores it in a file.
			 This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param Flags [in]

A value that specifies the type of certificate to create. This can be one of the following values.

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
PKCS 10

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V2_0"></a><a id="xecr_pkcs10_v2_0"></a><dl>
<dt><b>XECR_PKCS10_V2_0</b></dt>
</dl>
</td>
<td width="60%">
PKCS 10 version 2

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS7"></a><a id="xecr_pkcs7"></a><dl>
<dt><b>XECR_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
PKCS 7

</td>
</tr>
</table>

### -param strDNName [in]

This parameter can be <b>NULL</b>; otherwise, this parameter specifies the distinguished name (DN) of the entity for which the request is being made. The DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention, for example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an OID can be provided instead.

### -param strUsage [in]

An <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that describes the purpose of the request being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

### -param strRequestFileName [in]

The name of the file that will receive the request.

## -returns

<h3>VB</h3>
If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When this method is called from script, the method displays a user interface that asks whether the user will allow creation of a  certificate request and whether the user will allow a write operation to the file system.
