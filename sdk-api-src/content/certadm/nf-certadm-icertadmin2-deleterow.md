---
UID: NF:certadm.ICertAdmin2.DeleteRow
title: ICertAdmin2::DeleteRow (certadm.h)
description: The DeleteRow method deletes a row or set of rows from a database table. The caller specifies a database table and either a row ID or an ending date.
helpviewer_keywords: ["CCertAdmin object [Security]","DeleteRow method","CDR_EXPIRED","CDR_REQUEST_LAST_CHANGED","CVRC_TABLE_ATTRIBUTES","CVRC_TABLE_CRL","CVRC_TABLE_EXTENSIONS","CVRC_TABLE_REQCERT","DeleteRow","DeleteRow method [Security]","DeleteRow method [Security]","CCertAdmin object","DeleteRow method [Security]","ICertAdmin interface","DeleteRow method [Security]","ICertAdmin2 interface","ICertAdmin interface [Security]","DeleteRow method","ICertAdmin2 interface [Security]","DeleteRow method","ICertAdmin2.DeleteRow","ICertAdmin2::DeleteRow","ICertAdmin::DeleteRow","certadm/ICertAdmin2::DeleteRow","certadm/ICertAdmin::DeleteRow","security.icertadmin2_deleterow"]
old-location: security\icertadmin2_deleterow.htm
tech.root: security
ms.assetid: ee64740a-850b-4af5-a7cd-75eaa1687f8d
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],DeleteRow method, CDR_EXPIRED, CDR_REQUEST_LAST_CHANGED, CVRC_TABLE_ATTRIBUTES, CVRC_TABLE_CRL, CVRC_TABLE_EXTENSIONS, CVRC_TABLE_REQCERT, DeleteRow, DeleteRow method [Security], DeleteRow method [Security],CCertAdmin object, DeleteRow method [Security],ICertAdmin interface, DeleteRow method [Security],ICertAdmin2 interface, ICertAdmin interface [Security],DeleteRow method, ICertAdmin2 interface [Security],DeleteRow method, ICertAdmin2.DeleteRow, ICertAdmin2::DeleteRow, ICertAdmin::DeleteRow, certadm/ICertAdmin2::DeleteRow, certadm/ICertAdmin::DeleteRow, security.icertadmin2_deleterow
req.header: certadm.h
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
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin2::DeleteRow
 - certadm/ICertAdmin2::DeleteRow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.DeleteRow
 - ICertAdmin.DeleteRow
 - CCertAdmin.DeleteRow
---

# ICertAdmin2::DeleteRow


## -description

The <b>DeleteRow</b> method deletes a row or set of rows from a database table. The caller specifies a database table and either a row ID or an ending date.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>DeleteRow</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param Flags [in]

If not zero, specifies whether <i>Date</i> applies to an expiration date or a last modified date.


This can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CDR_EXPIRED"></a><a id="cdr_expired"></a><dl>
<dt><b>CDR_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The rows being deleted have an expiration date less than <i>Date</i>. This flag can be used when <i>Table</i> is  CVRC_TABLE_REQCERT or CVRC_TABLE_CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CDR_REQUEST_LAST_CHANGED"></a><a id="cdr_request_last_changed"></a><dl>
<dt><b>CDR_REQUEST_LAST_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The rows being deleted are for pending or denied requests, and their last modified date is less than <i>Date</i>. This flag can be used when <i>Table</i> is  CVRC_TABLE_REQCERT.

</td>
</tr>
</table>

### -param Date [in]

Specifies an expiration date when deleting certificates or CRLs, and a last modified date when deleting certificate requests.

If this value is not zero, then <i>RowID</i> must be zero.

### -param Table [in]

A <b>LONG</b> value that specifies the Certificate Services database table from which the rows are to be deleted.


This can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_ATTRIBUTES"></a><a id="cvrc_table_attributes"></a><dl>
<dt><b>CVRC_TABLE_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/a-gly">attributes</a> table is used.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_CRL"></a><a id="cvrc_table_crl"></a><dl>
<dt><b>CVRC_TABLE_CRL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) table is used.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_EXTENSIONS"></a><a id="cvrc_table_extensions"></a><dl>
<dt><b>CVRC_TABLE_EXTENSIONS</b></dt>
</dl>
</td>
<td width="60%">
The extensions table is used.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_REQCERT"></a><a id="cvrc_table_reqcert"></a><dl>
<dt><b>CVRC_TABLE_REQCERT</b></dt>
</dl>
</td>
<td width="60%">
The table of pending requests, denied requests, issued certificates, and revoked certificates is used.

</td>
</tr>
</table>

### -param RowId [in]

Specifies the ID of the row to delete.

If this value is not zero, then <i>Date</i> must be zero.

### -param pcDeleted [out]

The number of rows successfully deleted.

## -returns

<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful, and *<i>pcDeleted</i> is set to the number of rows deleted.

<h3>VB</h3>
The number of rows deleted.

## -remarks

<i>RowID</i> and <i>Date</i> are mutually exclusive; one and only one of them can be nonzero.

## -see-also

<b>CCertAdmin</b>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>