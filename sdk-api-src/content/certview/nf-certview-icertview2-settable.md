---
UID: NF:certview.ICertView2.SetTable
title: ICertView2::SetTable (certview.h)
description: Specifies which Certificate Services database table is used for subsequent calls to the methods of the ICertView2 interface.
helpviewer_keywords: ["CCertView object [Security]","SetTable method","CVRC_TABLE_ATTRIBUTES","CVRC_TABLE_CRL","CVRC_TABLE_EXTENSIONS","CVRC_TABLE_REQCERT","ICertView interface [Security]","SetTable method","ICertView2 interface [Security]","SetTable method","ICertView2.SetTable","ICertView2::SetTable","ICertView::SetTable","SetTable","SetTable method [Security]","SetTable method [Security]","CCertView object","SetTable method [Security]","ICertView interface","SetTable method [Security]","ICertView2 interface","_certsrv_icertview2_settable","certview/ICertView2::SetTable","certview/ICertView::SetTable","security.icertview2_settable"]
old-location: security\icertview2_settable.htm
tech.root: security
ms.assetid: 76353137-75c5-46e5-82da-33d2f8e54661
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],SetTable method, CVRC_TABLE_ATTRIBUTES, CVRC_TABLE_CRL, CVRC_TABLE_EXTENSIONS, CVRC_TABLE_REQCERT, ICertView interface [Security],SetTable method, ICertView2 interface [Security],SetTable method, ICertView2.SetTable, ICertView2::SetTable, ICertView::SetTable, SetTable, SetTable method [Security], SetTable method [Security],CCertView object, SetTable method [Security],ICertView interface, SetTable method [Security],ICertView2 interface, _certsrv_icertview2_settable, certview/ICertView2::SetTable, certview/ICertView::SetTable, security.icertview2_settable
req.header: certview.h
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
 - ICertView2::SetTable
 - certview/ICertView2::SetTable
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
 - ICertView2.SetTable
 - ICertView.SetTable
 - CCertView.SetTable
---

# ICertView2::SetTable


## -description

The <b>SetTable</b> method  specifies which Certificate Services database table is used for subsequent calls to  the methods of the <a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a> interface.

## -parameters

### -param Table [in]

Specifies the Certificate Services database table to use for subsequent calls. This parameter must be one of the following values. 




					

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
The <a href="/windows/desktop/SecGloss/a-gly">attributes</a> table is used for subsequent calls.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_CRL"></a><a id="cvrc_table_crl"></a><dl>
<dt><b>CVRC_TABLE_CRL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) table is used for subsequent calls.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_EXTENSIONS"></a><a id="cvrc_table_extensions"></a><dl>
<dt><b>CVRC_TABLE_EXTENSIONS</b></dt>
</dl>
</td>
<td width="60%">
The extensions table is used for subsequent calls.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_REQCERT"></a><a id="cvrc_table_reqcert"></a><dl>
<dt><b>CVRC_TABLE_REQCERT</b></dt>
</dl>
</td>
<td width="60%">
The table of pending requests, denied requests, issued certificates, and revoked certificates is used for subsequent calls.

</td>
</tr>
</table>

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Before calling the <b>SetTable</b> method, it is necessary to establish a connection with a Certificate Services server by calling the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a> method first. After the <b>OpenConnection</b> and <b>SetTable</b> calls are made, subsequent calls to the <a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a> interface methods will use the Certificate Services database table specified by the <b>SetTable</b> method.

If the <b>SetTable</b> method is not called, then the default table  CVRC_TABLE_REQCERT is used.


#### Examples


```cpp
HRESULT hr;

// Specify the certificate revocation list table.
hr = pCertView2->SetTable(CVRC_TABLE_CRL);
if (FAILED(hr))
{
    printf("Failed SetTable\n");
    exit(1);  // Or other error action.
}
```