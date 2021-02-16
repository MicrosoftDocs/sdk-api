---
UID: NS:wincrypt._CMC_STATUS_INFO
title: CMC_STATUS_INFO (wincrypt.h)
description: Contains status information about Certificate Management Messages over CMS.
helpviewer_keywords: ["*PCMC_STATUS_INFO","CMC_FAIL_BAD_ALG","CMC_FAIL_BAD_CERT_ID","CMC_FAIL_BAD_IDENTITY","CMC_FAIL_BAD_MESSAGE_CHECK","CMC_FAIL_BAD_REQUEST","CMC_FAIL_BAD_TIME","CMC_FAIL_INTERNAL_CA_ERROR","CMC_FAIL_MUST_ARCHIVE_KEYS","CMC_FAIL_NO_KEY_REUSE","CMC_FAIL_POP_FAILED","CMC_FAIL_POP_REQUIRED","CMC_FAIL_TRY_LATER","CMC_FAIL_UNSUPORTED_EXT","CMC_STATUS_CONFIRM_REQUIRED","CMC_STATUS_FAILED","CMC_STATUS_INFO","CMC_STATUS_INFO structure [Security]","CMC_STATUS_NO_SUPPORT","CMC_STATUS_PENDING","CMC_STATUS_SUCCESS","PCMC_STATUS_INFO","PCMC_STATUS_INFO structure pointer [Security]","_crypto2_cmc_status_info","security.cmc_status_info","wincrypt/CMC_STATUS_INFO","wincrypt/PCMC_STATUS_INFO"]
old-location: security\cmc_status_info.htm
tech.root: security
ms.assetid: 008f6de4-bad2-4c63-ba64-8d42ae71d50a
ms.date: 12/05/2018
ms.keywords: '*PCMC_STATUS_INFO, CMC_FAIL_BAD_ALG, CMC_FAIL_BAD_CERT_ID, CMC_FAIL_BAD_IDENTITY, CMC_FAIL_BAD_MESSAGE_CHECK, CMC_FAIL_BAD_REQUEST, CMC_FAIL_BAD_TIME, CMC_FAIL_INTERNAL_CA_ERROR, CMC_FAIL_MUST_ARCHIVE_KEYS, CMC_FAIL_NO_KEY_REUSE, CMC_FAIL_POP_FAILED, CMC_FAIL_POP_REQUIRED, CMC_FAIL_TRY_LATER, CMC_FAIL_UNSUPORTED_EXT, CMC_STATUS_CONFIRM_REQUIRED, CMC_STATUS_FAILED, CMC_STATUS_INFO, CMC_STATUS_INFO structure [Security], CMC_STATUS_NO_SUPPORT, CMC_STATUS_PENDING, CMC_STATUS_SUCCESS, PCMC_STATUS_INFO, PCMC_STATUS_INFO structure pointer [Security], _crypto2_cmc_status_info, security.cmc_status_info, wincrypt/CMC_STATUS_INFO, wincrypt/PCMC_STATUS_INFO'
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CMC_STATUS_INFO, *PCMC_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_STATUS_INFO
 - wincrypt/_CMC_STATUS_INFO
 - PCMC_STATUS_INFO
 - wincrypt/PCMC_STATUS_INFO
 - CMC_STATUS_INFO
 - wincrypt/CMC_STATUS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMC_STATUS_INFO
---

# CMC_STATUS_INFO structure


## -description

The <b>CMC_STATUS_INFO</b> structure contains status information about Certificate Management Messages over CMS.

## -struct-fields

### -field dwStatus

A <b>DWORD</b> value that indicates the status of the message.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMC_STATUS_SUCCESS"></a><a id="cmc_status_success"></a><dl>
<dt><b>CMC_STATUS_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Request was granted.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_STATUS_FAILED"></a><a id="cmc_status_failed"></a><dl>
<dt><b>CMC_STATUS_FAILED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Request failed. There is addition information in other parts of the message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_STATUS_PENDING"></a><a id="cmc_status_pending"></a><dl>
<dt><b>CMC_STATUS_PENDING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Request body part has not been processed. Requester must poll again. This value is returned only on <a href="/windows/desktop/SecGloss/c-gly">certificate requests</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_STATUS_NO_SUPPORT"></a><a id="cmc_status_no_support"></a><dl>
<dt><b>CMC_STATUS_NO_SUPPORT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Requested operation is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_STATUS_CONFIRM_REQUIRED"></a><a id="cmc_status_confirm_required"></a><dl>
<dt><b>CMC_STATUS_CONFIRM_REQUIRED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Confirmation by using the idConfirmCertAcceptance control is required before the certificate can be used.

</td>
</tr>
</table>

### -field cBodyList

A <b>DWORD</b> count of the elements in the <b>rgdwBodyList</b> array.

### -field rgdwBodyList

A <b>DWORD</b> array.

### -field pwszStatusString

Optional string text indicating message status.

### -field dwOtherInfoChoice

A <b>DWORD</b> value that identifies the union member to be used. 

This member can be one of the following values:

<ul>
<li>CMC_OTHER_INFO_NO_CHOICE</li>
<li>CMC_OTHER_INFO_FAIL_CHOICE</li>
<li>CMC_OTHER_INFO_PENDING_CHOICE</li>
</ul>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.dwFailInfo

A <b>DWORD</b> member of the union. This member is used if <b>dwOtherInfoChoice</b> is CMC_OTHER_INFO_FAIL_CHOICE. The following values are returned for various failures.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_ALG"></a><a id="cmc_fail_bad_alg"></a><dl>
<dt><b>CMC_FAIL_BAD_ALG</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unrecognized or unsupported algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_MESSAGE_CHECK"></a><a id="cmc_fail_bad_message_check"></a><dl>
<dt><b>CMC_FAIL_BAD_MESSAGE_CHECK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Integrity check failed.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_REQUEST"></a><a id="cmc_fail_bad_request"></a><dl>
<dt><b>CMC_FAIL_BAD_REQUEST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Transaction not permitted or supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_TIME"></a><a id="cmc_fail_bad_time"></a><dl>
<dt><b>CMC_FAIL_BAD_TIME</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Message time field was not sufficiently close to the system time.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_CERT_ID"></a><a id="cmc_fail_bad_cert_id"></a><dl>
<dt><b>CMC_FAIL_BAD_CERT_ID</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
No certificate could be identified matching the provided criteria.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_UNSUPORTED_EXT"></a><a id="cmc_fail_unsuported_ext"></a><dl>
<dt><b>CMC_FAIL_UNSUPORTED_EXT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Requested X.509 extension is not supported by the recipient CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_MUST_ARCHIVE_KEYS"></a><a id="cmc_fail_must_archive_keys"></a><dl>
<dt><b>CMC_FAIL_MUST_ARCHIVE_KEYS</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Private key material must be supplied.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_BAD_IDENTITY"></a><a id="cmc_fail_bad_identity"></a><dl>
<dt><b>CMC_FAIL_BAD_IDENTITY</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Identification attribute failed to verify.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_POP_REQUIRED"></a><a id="cmc_fail_pop_required"></a><dl>
<dt><b>CMC_FAIL_POP_REQUIRED</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Server requires a POP proof before issuing certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_POP_FAILED"></a><a id="cmc_fail_pop_failed"></a><dl>
<dt><b>CMC_FAIL_POP_FAILED</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
POP processing failed.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_NO_KEY_REUSE"></a><a id="cmc_fail_no_key_reuse"></a><dl>
<dt><b>CMC_FAIL_NO_KEY_REUSE</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Server policy does not allow key re-use.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_INTERNAL_CA_ERROR"></a><a id="cmc_fail_internal_ca_error"></a><dl>
<dt><b>CMC_FAIL_INTERNAL_CA_ERROR</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/c-gly">Certification authority</a> (CA) had an internal failure.

</td>
</tr>
<tr>
<td width="40%"><a id="CMC_FAIL_TRY_LATER"></a><a id="cmc_fail_try_later"></a><dl>
<dt><b>CMC_FAIL_TRY_LATER</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Request failed for an unknown reason. The request should be reissued later.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME.pPendInfo

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_pend_info">CMC_PEND_INFO</a> structure member of the union. This member is used if <b>dwOtherInfoChoice</b> is CMC_OTHER_INFO_PEND_CHOICE.

## -remarks

Additional members of the union may be defined in future versions.