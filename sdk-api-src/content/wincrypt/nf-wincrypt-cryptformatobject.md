---
UID: NF:wincrypt.CryptFormatObject
title: CryptFormatObject function (wincrypt.h)
description: The CryptFormatObject function formats the encoded data and returns a Unicode string in the allocated buffer according to the certificate encoding type.
helpviewer_keywords: ["0","CRYPT_FORMAT_STR_MULTI_LINE","CRYPT_FORMAT_STR_NO_HEX","CryptFormatObject","CryptFormatObject function [Security]","SPC_FINANCIAL_CRITERIA_OBJID","SPC_SP_AGENCY_INFO_OBJID","_crypto2_cryptformatobject","security.cryptformatobject","szOID_AUTHORITY_INFO_ACCESS","szOID_AUTHORITY_KEY_IDENTIFIER2","szOID_BASIC_CONSTRAINTS2","szOID_CERT_POLICIES","szOID_CRL_DIST_POINTS","szOID_CRL_REASON_CODE","szOID_ENHANCED_KEY_USAGE","szOID_ISSUER_ALT_NAME2","szOID_KEY_ATTRIBUTES","szOID_KEY_USAGE","szOID_KEY_USAGE_RESTRICTION","szOID_NEXT_UPDATE_LOCATION","szOID_RSA_SMIMECapabilities","szOID_SUBJECT_ALT_NAME2","szOID_SUBJECT_KEY_IDENTIFIER","wincrypt/CryptFormatObject"]
old-location: security\cryptformatobject.htm
tech.root: security
ms.assetid: 307e0bd5-b8a6-4d85-9775-65aae99e8dc6
ms.date: 12/05/2018
ms.keywords: 0, CRYPT_FORMAT_STR_MULTI_LINE, CRYPT_FORMAT_STR_NO_HEX, CryptFormatObject, CryptFormatObject function [Security], SPC_FINANCIAL_CRITERIA_OBJID, SPC_SP_AGENCY_INFO_OBJID, _crypto2_cryptformatobject, security.cryptformatobject, szOID_AUTHORITY_INFO_ACCESS, szOID_AUTHORITY_KEY_IDENTIFIER2, szOID_BASIC_CONSTRAINTS2, szOID_CERT_POLICIES, szOID_CRL_DIST_POINTS, szOID_CRL_REASON_CODE, szOID_ENHANCED_KEY_USAGE, szOID_ISSUER_ALT_NAME2, szOID_KEY_ATTRIBUTES, szOID_KEY_USAGE, szOID_KEY_USAGE_RESTRICTION, szOID_NEXT_UPDATE_LOCATION, szOID_RSA_SMIMECapabilities, szOID_SUBJECT_ALT_NAME2, szOID_SUBJECT_KEY_IDENTIFIER, wincrypt/CryptFormatObject
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptFormatObject
 - wincrypt/CryptFormatObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptFormatObject
---

# CryptFormatObject function


## -description

The <b>CryptFormatObject</b> function formats the encoded data and returns a Unicode string in the allocated buffer according to the certificate encoding type.

## -parameters

### -param dwCertEncodingType [in]

Type of encoding used on the certificate. The currently defined certificate encoding type used is X509_ASN_ENCODING.

### -param dwFormatType [in]

Format type values. Not used. Set to zero.

### -param dwFormatStrType [in]

Structure format type values. This parameter can be zero, or you can specify one or more of the following flags by using the bitwise-<b>OR</b> operator to combine them.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Display the data in a single line. Each subfield is concatenated with a comma (,). For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FORMAT_STR_MULTI_LINE"></a><a id="crypt_format_str_multi_line"></a><dl>
<dt><b>CRYPT_FORMAT_STR_MULTI_LINE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Display the data in multiple lines rather than single line (the default). For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FORMAT_STR_NO_HEX"></a><a id="crypt_format_str_no_hex"></a><dl>
<dt><b>CRYPT_FORMAT_STR_NO_HEX</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Disables the hexadecimal dump. For more information, see Remarks.

</td>
</tr>
</table>

### -param pFormatStruct [in]

A pointer to the format of the structure. Not used. Set to <b>NULL</b>.

### -param lpszStructType [in]

A pointer to an OID that defines the encoded data. If the high-order word of the <i>lpszStructType</i> parameter is zero, the low-order word specifies the integer identifier for the type of the given structure. Otherwise, this parameter is a long pointer to a <b>null</b>-terminated string. 




The following table lists supported OIDs with their associated OID extension.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPC_FINANCIAL_CRITERIA_OBJID"></a><a id="spc_financial_criteria_objid"></a><dl>
<dt><b>SPC_FINANCIAL_CRITERIA_OBJID</b></dt>
</dl>
</td>
<td width="60%">
1.3.6.1.4.1.311.2.1.27

</td>
</tr>
<tr>
<td width="40%"><a id="SPC_SP_AGENCY_INFO_OBJID"></a><a id="spc_sp_agency_info_objid"></a><dl>
<dt><b>SPC_SP_AGENCY_INFO_OBJID</b></dt>
</dl>
</td>
<td width="60%">
1.3.6.1.4.1.311.2.1.10

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_AUTHORITY_INFO_ACCESS"></a><a id="szoid_authority_info_access"></a><a id="SZOID_AUTHORITY_INFO_ACCESS"></a><dl>
<dt><b>szOID_AUTHORITY_INFO_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
1.3.6.1.5.5.7.1.1

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_AUTHORITY_KEY_IDENTIFIER2"></a><a id="szoid_authority_key_identifier2"></a><a id="SZOID_AUTHORITY_KEY_IDENTIFIER2"></a><dl>
<dt><b>szOID_AUTHORITY_KEY_IDENTIFIER2</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.35

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_BASIC_CONSTRAINTS2"></a><a id="szoid_basic_constraints2"></a><a id="SZOID_BASIC_CONSTRAINTS2"></a><dl>
<dt><b>szOID_BASIC_CONSTRAINTS2</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.19

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CERT_POLICIES"></a><a id="szoid_cert_policies"></a><a id="SZOID_CERT_POLICIES"></a><dl>
<dt><b>szOID_CERT_POLICIES</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.32

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CRL_DIST_POINTS"></a><a id="szoid_crl_dist_points"></a><a id="SZOID_CRL_DIST_POINTS"></a><dl>
<dt><b>szOID_CRL_DIST_POINTS</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.31

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CRL_REASON_CODE"></a><a id="szoid_crl_reason_code"></a><a id="SZOID_CRL_REASON_CODE"></a><dl>
<dt><b>szOID_CRL_REASON_CODE</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.21

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_ENHANCED_KEY_USAGE"></a><a id="szoid_enhanced_key_usage"></a><a id="SZOID_ENHANCED_KEY_USAGE"></a><dl>
<dt><b>szOID_ENHANCED_KEY_USAGE</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.37

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_ISSUER_ALT_NAME2"></a><a id="szoid_issuer_alt_name2"></a><a id="SZOID_ISSUER_ALT_NAME2"></a><dl>
<dt><b>szOID_ISSUER_ALT_NAME2</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.18

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_KEY_ATTRIBUTES"></a><a id="szoid_key_attributes"></a><a id="SZOID_KEY_ATTRIBUTES"></a><dl>
<dt><b>szOID_KEY_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.2

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_KEY_USAGE"></a><a id="szoid_key_usage"></a><a id="SZOID_KEY_USAGE"></a><dl>
<dt><b>szOID_KEY_USAGE</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.15

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_KEY_USAGE_RESTRICTION"></a><a id="szoid_key_usage_restriction"></a><a id="SZOID_KEY_USAGE_RESTRICTION"></a><dl>
<dt><b>szOID_KEY_USAGE_RESTRICTION</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.4

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_NEXT_UPDATE_LOCATION"></a><a id="szoid_next_update_location"></a><a id="SZOID_NEXT_UPDATE_LOCATION"></a><dl>
<dt><b>szOID_NEXT_UPDATE_LOCATION</b></dt>
</dl>
</td>
<td width="60%">
1.3.6.1.4.1.311.10.2

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_RSA_SMIMECapabilities"></a><a id="szoid_rsa_smimecapabilities"></a><a id="SZOID_RSA_SMIMECAPABILITIES"></a><dl>
<dt><b>szOID_RSA_SMIMECapabilities</b></dt>
</dl>
</td>
<td width="60%">
1.2.840.113549.1.9.15

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SUBJECT_ALT_NAME2"></a><a id="szoid_subject_alt_name2"></a><a id="SZOID_SUBJECT_ALT_NAME2"></a><dl>
<dt><b>szOID_SUBJECT_ALT_NAME2</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.17

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SUBJECT_KEY_IDENTIFIER"></a><a id="szoid_subject_key_identifier"></a><a id="SZOID_SUBJECT_KEY_IDENTIFIER"></a><dl>
<dt><b>szOID_SUBJECT_KEY_IDENTIFIER</b></dt>
</dl>
</td>
<td width="60%">
2.5.29.14

</td>
</tr>
</table>

### -param pbEncoded [in]

A pointer to the encoded data to be formatted. If <i>lpszStructType</i> is one of the OIDs listed above, the <i>pbEncoded</i> is the encoded extension.

### -param cbEncoded [in]

The size, in bytes, of the <i>pbEncoded</i> structure.

### -param pbFormat [out]

A pointer to a buffer that receives the formatted string. When the buffer that is specified is not large enough to receive the decoded structure, the function sets ERROR_MORE_DATA and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbFormat</i>. This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see <a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbFormat [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbFormat</i> parameter. When the function returns, the variable pointed to by the <i>pcbFormat</i> parameter contains the number of bytes stored in the buffer. This parameter can be <b>NULL</b>, only if <i>pbFormat</i> is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size may be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit into the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If it does not succeed, the return value is <b>FALSE</b>. To retrieve extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The default behavior of this function is to return a single-line display of the encoded data, that is, each subfield is concatenated with a comma (,) on one line. If you prefer to display the data in multiple lines, set the CRYPT_FORMAT_STR_MULTI_LINE flag. Each subfield will then be displayed on a separate line.

If there is no formatting routine installed or registered for the <i>lpszStructType</i> parameter, the hexadecimal dump of the encoded 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> will be returned. A user can set the CRYPT_FORMAT_STR_NO_HEX flag to disable the hexadecimal dump.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>