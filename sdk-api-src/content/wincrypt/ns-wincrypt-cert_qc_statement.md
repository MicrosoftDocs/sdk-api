---
UID: NS:wincrypt._CERT_QC_STATEMENT
title: CERT_QC_STATEMENT (wincrypt.h)
description: Represents a single statement in a sequence of one or more statements for inclusion in a Qualified Certificate (QC) statements extension.
helpviewer_keywords: ["*PCERT_QC_STATEMENT","CERT_QC_STATEMENT","CERT_QC_STATEMENT structure [Security]","PCERT_QC_STATEMENT","PCERT_QC_STATEMENT structure pointer [Security]","security.cert_qc_statement","szOID_QC_EU_COMPLIANCE","szOID_QC_SSCD","wincrypt/CERT_QC_STATEMENT","wincrypt/PCERT_QC_STATEMENT"]
old-location: security\cert_qc_statement.htm
tech.root: security
ms.assetid: e163da81-d854-4f56-8eef-2788f1b566ba
ms.date: 12/05/2018
ms.keywords: '*PCERT_QC_STATEMENT, CERT_QC_STATEMENT, CERT_QC_STATEMENT structure [Security], PCERT_QC_STATEMENT, PCERT_QC_STATEMENT structure pointer [Security], security.cert_qc_statement, szOID_QC_EU_COMPLIANCE, szOID_QC_SSCD, wincrypt/CERT_QC_STATEMENT, wincrypt/PCERT_QC_STATEMENT'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_QC_STATEMENT, *PCERT_QC_STATEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_QC_STATEMENT
 - wincrypt/_CERT_QC_STATEMENT
 - PCERT_QC_STATEMENT
 - wincrypt/PCERT_QC_STATEMENT
 - CERT_QC_STATEMENT
 - wincrypt/CERT_QC_STATEMENT
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
 - CERT_QC_STATEMENT
---

# CERT_QC_STATEMENT structure


## -description

The <b>CERT_QC_STATEMENT</b> structure represents a single statement in a sequence of one or more statements for inclusion in a  Qualified Certificate (QC) statements extension. This structure populates the <b>rgStatement</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_qc_statements_ext_info">CERT_QC_STATEMENTS_EXT_INFO</a> structure.

## -struct-fields

### -field pszStatementId

A pointer to a string that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the defined statement.


The Wincrypt.h file defines the following <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) for use with this member, but this member can be any OID as required by an application.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_QC_EU_COMPLIANCE"></a><a id="szoid_qc_eu_compliance"></a><a id="SZOID_QC_EU_COMPLIANCE"></a><dl>
<dt><b>szOID_QC_EU_COMPLIANCE</b></dt>
<dt>"0.4.0.1862.1.1"</dt>
</dl>
</td>
<td width="60%">
European Union

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_QC_SSCD"></a><a id="szoid_qc_sscd"></a><a id="SZOID_QC_SSCD"></a><dl>
<dt><b>szOID_QC_SSCD</b></dt>
<dt>"0.4.0.1862.1.4"</dt>
</dl>
</td>
<td width="60%">
Secure Signature Creation Device

</td>
</tr>
</table>

### -field StatementInfo

An optional <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains additional information that qualifies the defined statement. The <b>pszStatementId</b> member defines the syntax of this parameter.