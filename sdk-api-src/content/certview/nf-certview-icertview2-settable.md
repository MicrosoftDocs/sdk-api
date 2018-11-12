---
UID: NF:certview.ICertView2.SetTable
title: ICertView2::SetTable
author: windows-sdk-content
description: Specifies which Certificate Services database table is used for subsequent calls to the methods of the ICertView2 interface.
old-location: security\icertview2_settable.htm
tech.root: seccrypto
ms.assetid: 76353137-75c5-46e5-82da-33d2f8e54661
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertView object [Security],SetTable method, CVRC_TABLE_ATTRIBUTES, CVRC_TABLE_CRL, CVRC_TABLE_EXTENSIONS, CVRC_TABLE_REQCERT, ICertView interface [Security],SetTable method, ICertView2 interface [Security],SetTable method, ICertView2.SetTable, ICertView2::SetTable, ICertView::SetTable, SetTable, SetTable method [Security], SetTable method [Security],CCertView object, SetTable method [Security],ICertView interface, SetTable method [Security],ICertView2 interface, _certsrv_icertview2_settable, certview/ICertView2::SetTable, certview/ICertView::SetTable, security.icertview2_settable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView2::SetTable


## -description


The <b>SetTable</b> method  specifies which Certificate Services database table is used for subsequent calls to  the methods of the <a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a> interface.


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
The <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> table is used for subsequent calls.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_TABLE_CRL"></a><a id="cvrc_table_crl"></a><dl>
<dt><b>CVRC_TABLE_CRL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) table is used for subsequent calls.

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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Before calling the <b>SetTable</b> method, it is necessary to establish a connection with a Certificate Services server by calling the 
<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">OpenConnection</a> method first. After the <b>OpenConnection</b> and <b>SetTable</b> calls are made, subsequent calls to the <a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a> interface methods will use the Certificate Services database table specified by the <b>SetTable</b> method.

If the <b>SetTable</b> method is not called, then the default table  CVRC_TABLE_REQCERT is used.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;

// Specify the certificate revocation list table.
hr = pCertView2-&gt;SetTable(CVRC_TABLE_CRL);
if (FAILED(hr))
{
    printf("Failed SetTable\n");
    exit(1);  // Or other error action.
}</pre>
</td>
</tr>
</table></span></div>


