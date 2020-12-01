---
UID: NF:certadm.ICertAdmin.ImportCertificate
title: ICertAdmin::ImportCertificate (certadm.h)
description: Takes a previously issued certificate and imports it to the certification authority's (CA) database. This method was first defined in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin object [Security]","ImportCertificate method","CR_IN_BASE64","CR_IN_BASE64HEADER","CR_IN_BINARY","ICertAdmin interface [Security]","ImportCertificate method","ICertAdmin.ImportCertificate","ICertAdmin2 interface [Security]","ImportCertificate method","ICertAdmin2::ImportCertificate","ICertAdmin::ImportCertificate","ImportCertificate","ImportCertificate method [Security]","ImportCertificate method [Security]","CCertAdmin object","ImportCertificate method [Security]","ICertAdmin interface","ImportCertificate method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::ImportCertificate","certadm/ICertAdmin::ImportCertificate","security.icertadmin2_importcertificate"]
old-location: security\icertadmin2_importcertificate.htm
tech.root: security
ms.assetid: b79a726e-5823-468b-869d-382e6fd73b44
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],ImportCertificate method, CR_IN_BASE64, CR_IN_BASE64HEADER, CR_IN_BINARY, ICertAdmin interface [Security],ImportCertificate method, ICertAdmin.ImportCertificate, ICertAdmin2 interface [Security],ImportCertificate method, ICertAdmin2::ImportCertificate, ICertAdmin::ImportCertificate, ImportCertificate, ImportCertificate method [Security], ImportCertificate method [Security],CCertAdmin object, ImportCertificate method [Security],ICertAdmin interface, ImportCertificate method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::ImportCertificate, certadm/ICertAdmin::ImportCertificate, security.icertadmin2_importcertificate
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
 - ICertAdmin::ImportCertificate
 - certadm/ICertAdmin::ImportCertificate
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
 - ICertAdmin2.ImportCertificate
 - ICertAdmin.ImportCertificate
 - CCertAdmin.ImportCertificate
---

# ICertAdmin::ImportCertificate


## -description

The <b>ImportCertificate</b> method takes a previously issued certificate and imports it to the <a href="/windows/desktop/SecGloss/c-gly">certification authority's</a> (CA) database. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

 For the requirements that the certificate must meet to be successfully imported, see  Remarks.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the certification authority in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>ImportCertificate</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param strCertificate [in]

The binary representation of the certificate being imported.

### -param Flags [in]

Specifies the format of the certificate. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64HEADER"></a><a id="cr_in_base64header"></a><dl>
<dt><b>CR_IN_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64"></a><a id="cr_in_base64"></a><dl>
<dt><b>CR_IN_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BINARY"></a><a id="cr_in_binary"></a><dl>
<dt><b>CR_IN_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>

### -param pRequestId [out]

A pointer to a <b>LONG</b> value that receives the database-assigned request ID for the imported certificate.

## -returns

<h3>C++</h3>
 If the method succeeds, and the <i>pRequestID</i> parameter is set to the value of the database-assigned request ID for the imported certificate, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the database-assigned request ID for the imported certificate.

## -remarks

The <b>ImportCertificate</b> method is useful in the case of a certification authority that has been partially restored from backup: If a certificate is not on the backup tapes used to restore the certification authority but exists in a file, the certificate can be imported by means of this method.

For this method to succeed, the certificate being imported must have been previously issued by the certification authority specified in <i>strConfig</i>. The restored certification authority will validate the certificate's signature, and if the signature is not valid, the method call will fail.

Furthermore, you cannot import a certificate if it already exists in the database. Each certificate in the database must be unique. The database ensures uniqueness by checking the certificate's serial number.


#### Examples


```cpp
// This code imports a binary certificate file.
BSTR   bstrCert = NULL;  // Variable for certificate.
HANDLE hFile;  
DWORD  cchFile, cbRead;
LONG   nID;  // Variable for request ID.

// Open the file that contains the certificate.
hFile = CreateFile((LPCSTR) "d:\\cert1.cer",
                  GENERIC_READ,
                  FILE_SHARE_READ,
                  NULL,
                  OPEN_EXISTING,
                  0,
                  NULL);
if (INVALID_HANDLE_VALUE == hFile)
{
    printf("Unable to open file\n");
    // Take error action as needed.
}
// Determine the file size.
cchFile = GetFileSize(hFile, NULL);
if ( (DWORD)-1 == cchFile )
{
    printf("Failed GetFileSize\n");
    CloseHandle(hFile);
    // Take error action as needed.
}
// Allocate the memory for the certificate.
bstrCert = SysAllocStringByteLen(NULL, cchFile);
if (NULL == bstrCert)
{
    printf("Failed SysAllocStringByteLen\n");
    CloseHandle(hFile);
    // Take error action as needed.
}
// Read in the certificate.
if (!ReadFile(hFile,
             (char *)bstrCert,
             cchFile,
             &cbRead,
             NULL) || (cbRead != cchFile))
{
    printf("Failed to successfully read file\n");
    CloseHandle(hFile);
    SysFreeString(bstrCert);
    // Take error action as needed.
}
// Close the file.
CloseHandle(hFile);

// Import the certificate.
bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
if (FAILED(hr))
{
    printf("Failed to allocate memory for bstrCA\n");
    SysFreeString(bstrCert);
    // Take error action as needed.
}

hr = pCertAdmin->ImportCertificate(bstrCA,
                                   bstrCert,
                                   CR_IN_BINARY,
                                   &nID);
if (FAILED(hr))
    printf("Failed ImportCertificate [%x]\n", hr);
else
    printf("Imported certificated has Request ID: %d\n", nID);

SysFreeString(bstrCert);
SysFreeString(bstrCA);
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>