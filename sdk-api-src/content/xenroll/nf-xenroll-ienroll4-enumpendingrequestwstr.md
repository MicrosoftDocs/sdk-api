---
UID: NF:xenroll.IEnroll4.enumPendingRequestWStr
title: IEnroll4::enumPendingRequestWStr (xenroll.h)
description: Enumerates pending certificate requests and retrieves a specified property from each.
helpviewer_keywords: ["IEnroll4 interface [Security]","enumPendingRequestWStr method","IEnroll4.enumPendingRequestWStr","IEnroll4::enumPendingRequestWStr","XEPR_CADNS","XEPR_CAFRIENDLYNAME","XEPR_CANAME","XEPR_HASH","XEPR_REQUESTID","enumPendingRequestWStr","enumPendingRequestWStr method [Security]","enumPendingRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_enumpendingrequestwstr","xenroll/IEnroll4::enumPendingRequestWStr"]
old-location: security\ienroll4_enumpendingrequestwstr.htm
tech.root: security
ms.assetid: ae1ac12c-0332-4796-8269-a3b6f72b8bff
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],enumPendingRequestWStr method, IEnroll4.enumPendingRequestWStr, IEnroll4::enumPendingRequestWStr, XEPR_CADNS, XEPR_CAFRIENDLYNAME, XEPR_CANAME, XEPR_HASH, XEPR_REQUESTID, enumPendingRequestWStr, enumPendingRequestWStr method [Security], enumPendingRequestWStr method [Security],IEnroll4 interface, security.ienroll4_enumpendingrequestwstr, xenroll/IEnroll4::enumPendingRequestWStr
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
 - IEnroll4::enumPendingRequestWStr
 - xenroll/IEnroll4::enumPendingRequestWStr
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
 - IEnroll4.enumPendingRequestWStr
---

# IEnroll4::enumPendingRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumPendingRequestWStr</b> method enumerates pending <a href="/windows/desktop/SecGloss/c-gly">certificate requests</a> and retrieves a specified property from each.  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param lIndex [in]

Specifies the ordinal position of the pending request whose property will be retrieved. Specify zero for the first request.

### -param lDesiredProperty [in]

Identifier for the property being retrieved. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEPR_CADNS"></a><a id="xepr_cadns"></a><dl>
<dt><b>XEPR_CADNS</b></dt>
</dl>
</td>
<td width="60%">
DNS name for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA).

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CAFRIENDLYNAME"></a><a id="xepr_cafriendlyname"></a><dl>
<dt><b>XEPR_CAFRIENDLYNAME</b></dt>
</dl>
</td>
<td width="60%">
Display name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CANAME"></a><a id="xepr_caname"></a><dl>
<dt><b>XEPR_CANAME</b></dt>
</dl>
</td>
<td width="60%">
Name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_HASH"></a><a id="xepr_hash"></a><dl>
<dt><b>XEPR_HASH</b></dt>
</dl>
</td>
<td width="60%">
Hash value of the request.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_REQUESTID"></a><a id="xepr_requestid"></a><dl>
<dt><b>XEPR_REQUESTID</b></dt>
</dl>
</td>
<td width="60%">
Certificate request ID.

</td>
</tr>
</table>

### -param ppProperty [out]

A pointer to a <b>VOID</b> that receives the value of the retrieved property.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.


If the following values are specified for <i>lDesiredProperty</i>, this method returns E_NOTIMPL:

<ul>
<li>XEPR_DATE</li>
<li>XEPR_V1TEMPLATENAME</li>
<li>XEPR_V2TEMPLATEOID</li>
<li>XEPR_VERSION</li>
</ul>


If you specify any other value for <i>lDesiredProperty</i>, this method returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>