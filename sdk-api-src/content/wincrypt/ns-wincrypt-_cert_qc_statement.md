---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CERT_QC_STATEMENT structure


## -description


The <b>CERT_QC_STATEMENT</b> structure represents a single statement in a sequence of one or more statements for inclusion in a  Qualified Certificate (QC) statements extension. This structure populates the <b>rgStatement</b> member of the <a href="https://msdn.microsoft.com/788b3848-8d38-4e8f-9fdb-452767fbac61">CERT_QC_STATEMENTS_EXT_INFO</a> structure.


## -struct-fields




### -field pszStatementId

A pointer to a string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the defined statement.


The Wincrypt.h file defines the following <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) for use with this member, but this member can be any OID as required by an application.



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

An optional <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains additional information that qualifies the defined statement. The <b>pszStatementId</b> member defines the syntax of this parameter.

