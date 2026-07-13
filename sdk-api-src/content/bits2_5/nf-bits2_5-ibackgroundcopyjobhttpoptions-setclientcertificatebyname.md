---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.SetClientCertificateByName
title: IBackgroundCopyJobHttpOptions::SetClientCertificateByName (bits2_5.h)
description: Specifies the subject name of the client certificate to use for client authentication in an HTTPS (SSL) request.
helpviewer_keywords: ["CA","IBackgroundCopyJobHttpOptions interface [BITS]","SetClientCertificateByName method","IBackgroundCopyJobHttpOptions.SetClientCertificateByName","IBackgroundCopyJobHttpOptions::SetClientCertificateByName","MY","ROOT","SPC","SetClientCertificateByName","SetClientCertificateByName method [BITS]","SetClientCertificateByName method [BITS]","IBackgroundCopyJobHttpOptions interface","bits.ibackgroundcopyjobhttpoptions_setclientcertificatebyname","bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByName"]
old-location: bits\ibackgroundcopyjobhttpoptions_setclientcertificatebyname.htm
tech.root: Bits
ms.assetid: 8262b360-ab05-42a3-b5e7-178dc9f23fc6
ms.date: 12/05/2018
ms.keywords: CA, IBackgroundCopyJobHttpOptions interface [BITS],SetClientCertificateByName method, IBackgroundCopyJobHttpOptions.SetClientCertificateByName, IBackgroundCopyJobHttpOptions::SetClientCertificateByName, MY, ROOT, SPC, SetClientCertificateByName, SetClientCertificateByName method [BITS], SetClientCertificateByName method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_setclientcertificatebyname, bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByName
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions::SetClientCertificateByName
 - bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions.SetClientCertificateByName
---

# IBackgroundCopyJobHttpOptions::SetClientCertificateByName


## -description

Specifies the subject name of the client certificate to use for client authentication in an HTTPS (SSL) request.

## -parameters

### -param StoreLocation [in]

Identifies the location of a system store to use for looking up the certificate. For possible values, see the <a href="/windows/win32/api/bits2_5/ne-bits2_5-bg_cert_store_location">BG_CERT_STORE_LOCATION</a> enumeration.

### -param StoreName [in]

Null-terminated string that contains the name of the certificate store. The string is limited to 256 characters, including the null terminator. You can specify one of the following system stores or an application-defined store. The store can be a local or remote store. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CA"></a><a id="ca"></a><dl>
<dt><b>CA</b></dt>
</dl>
</td>
<td width="60%">
Certification authority certificates

</td>
</tr>
<tr>
<td width="40%"><a id="MY"></a><a id="my"></a><dl>
<dt><b>MY</b></dt>
</dl>
</td>
<td width="60%">
Personal certificates

</td>
</tr>
<tr>
<td width="40%"><a id="ROOT"></a><a id="root"></a><dl>
<dt><b>ROOT</b></dt>
</dl>
</td>
<td width="60%">
Root certificates

</td>
</tr>
<tr>
<td width="40%"><a id="SPC"></a><a id="spc"></a><dl>
<dt><b>SPC</b></dt>
</dl>
</td>
<td width="60%">
Software Publisher Certificate

</td>
</tr>
</table>

### -param SubjectName [in]

Null-terminated string that contains the simple subject name of the certificate. If the subject name contains multiple relative distinguished names (RDNs), you can specify one or more adjacent RDNs. If you specify more than one RDN, the list is comma-delimited. The string is limited to 256 characters, including the null terminator. You cannot specify an empty subject name. 

Do not include the object identifier in the name. You must specify the RDNs in the reverse order from what the certificate displays. For example, if the subject name in the certificate is "CN=name1, OU=name2, O=name3", specify the subject name as "name3, name2, name1".

## -returns

The following table lists some of the possible return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have permission to access the store location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>StoreLocation</i> is not defined in the <a href="/windows/win32/api/bits2_5/ne-bits2_5-bg_cert_store_location">BG_CERT_STORE_LOCATION</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Could not find a store matching the value of the <i>StoreName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A certificate matching the subject name was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_NULL_REF_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>StoreName</i> or <i>SubjectName</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The <i>StoreName</i> or <i>SubjectName</i> parameter is more than 256 characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -remarks

Only the job owner can specify the client certificate. If the job changes ownership, BITS removes the certificate from the job.

The client certificate is applicable only for remote files that use the HTTP or HTTPS protocol. You can specify a certificate for all job types.

When a website accepts but does not require an SSL client certificate, and the BITS job does not specify a client certificate, the job will fail with ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED (0x80072f0c).

The method uses the subject name string to perform a substring search for the certificate. Since subject names are not necessarily unique, this method searches the store for the first certificate that uses the given subject name and is a client authentication certificate. You should provide the complete subject name for a better chance of finding a single match. If the certificate is not correct (not trusted), the job will fail with BG_E_HTTP_ERROR_403 when BITS tries to transfer the file and the job will move to the error state. If you cannot guarantee a unique subject name, consider using the <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a> method instead.

SmartCard certificate identifiers (thumbprints) are not supported.


#### Examples

The following example shows how to specify a client certificate for a job by using the subject name of the certificate.   The example assumes that pJob points to a valid job.


```cpp

  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;

  // Change list of names to actual list of names.
  LPWSTR pSubjectName = L"name3, name2, name1";  
                                                    
  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&pHttpOptions);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }

  // Use the client certificate in the current user's personal (MY) store.
  hr = pHttpOptions->SetClientCertificateByName(BG_CERT_STORE_LOCATION_CURRENT_USER, 
                                      L"MY", pSubjectName));
  if (FAILED(hr))
  {
    wprintf(L"pHttpOptions->SetClientCertificateByName failed with 0x%x.\n", hr);
    goto cleanup;
  }


cleanup:

  if (pHttpOptions)
  {
    hr = pHttpOptions->Release();
  }

```

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getclientcertificate">IBackgroundCopyJobHttpOptions::GetClientCertificate</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-removeclientcertificate">IBackgroundCopyJobHttpOptions::RemoveClientCertificate</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>