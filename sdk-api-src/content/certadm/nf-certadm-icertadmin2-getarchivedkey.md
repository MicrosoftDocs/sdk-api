---
UID: NF:certadm.ICertAdmin2.GetArchivedKey
title: ICertAdmin2::GetArchivedKey
author: windows-sdk-content
description: Retrieves an archived key recovery BLOB.
old-location: security\icertadmin2_getarchivedkey.htm
old-project: SecCrypto
ms.assetid: 2da85485-99ef-4381-888b-f0ac930b70dc
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CCertAdmin object [Security],GetArchivedKey method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CV_OUT_BINARY, GetArchivedKey, GetArchivedKey method [Security], GetArchivedKey method [Security],CCertAdmin object, GetArchivedKey method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetArchivedKey method, ICertAdmin2.GetArchivedKey, ICertAdmin2::GetArchivedKey, _certsrv_icertadmin2_getarchivedkey, certadm/ICertAdmin2::GetArchivedKey, security.icertadmin2_getarchivedkey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetArchivedKey
 - CCertAdmin.GetArchivedKey
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# ICertAdmin2::GetArchivedKey


## -description


The <b>GetArchivedKey</b> method retrieves an archived key recovery <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>. This method was first defined in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) in the form <i>ComputerName</i>\<i>CAName</i>, where <i>ComputerName</i> is the Certificate Services server's network name, and <i>CAName</i> is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>GetArchivedKey</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Represents the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> ID in the Certificates Services database.


### -param Flags [in]

The following flags can be used to specify the format of the returned BLOB. 




               

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64"></a><a id="cr_out_base64"></a><dl>
<dt><b>CR_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 without BEGIN/END

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64HEADER"></a><a id="cr_out_base64header"></a><dl>
<dt><b>CR_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN CERTIFICATE and END CERTIFICATE

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BINARY"></a><a id="cv_out_binary"></a><dl>
<dt><b>CV_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary

</td>
</tr>
</table>
 


### -param pstrArchivedKey [out]

A pointer to the string that represents the retrieved archived <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>. When you have finished using this string, it is the responsibility of the caller to free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.


## -returns



<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates the method was successful.

<h3>VB</h3>
A string that contains the retrieved archived key BLOB.




## -remarks



An archived key is encrypted in a PKCS #7 to the key recovery agent certificate or certificates, and is stored in the Certificate Services database in that form. This method retrieves the encrypted PKCS #7 from the Certificate Services database, wraps it in a signed PKCS #7 which contains the user certificate and chain, the key recovery agent certificate or certificates, and the certification authority's signing certificate and chain. An authenticated attribute contains a certificate used to uniquely identify the user certificate.



