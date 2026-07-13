---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.SetClientCertificateByID
title: IBackgroundCopyJobHttpOptions::SetClientCertificateByID (bits2_5.h)
description: Specifies the identifier of the client certificate to use for client authentication in an HTTPS (SSL) request.
helpviewer_keywords: ["CA","IBackgroundCopyJobHttpOptions interface [BITS]","SetClientCertificateByID method","IBackgroundCopyJobHttpOptions.SetClientCertificateByID","IBackgroundCopyJobHttpOptions::SetClientCertificateByID","MY","ROOT","SPC","SetClientCertificateByID","SetClientCertificateByID method [BITS]","SetClientCertificateByID method [BITS]","IBackgroundCopyJobHttpOptions interface","bits.ibackgroundcopyjobhttpoptions_setclientcertificatebyid","bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByID"]
old-location: bits\ibackgroundcopyjobhttpoptions_setclientcertificatebyid.htm
tech.root: Bits
ms.assetid: 60839bac-7f5f-4c43-84d4-26f1b21f974d
ms.date: 12/05/2018
ms.keywords: CA, IBackgroundCopyJobHttpOptions interface [BITS],SetClientCertificateByID method, IBackgroundCopyJobHttpOptions.SetClientCertificateByID, IBackgroundCopyJobHttpOptions::SetClientCertificateByID, MY, ROOT, SPC, SetClientCertificateByID, SetClientCertificateByID method [BITS], SetClientCertificateByID method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_setclientcertificatebyid, bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByID
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
 - IBackgroundCopyJobHttpOptions::SetClientCertificateByID
 - bits2_5/IBackgroundCopyJobHttpOptions::SetClientCertificateByID
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
 - IBackgroundCopyJobHttpOptions.SetClientCertificateByID
---

# IBackgroundCopyJobHttpOptions::SetClientCertificateByID


## -description

Specifies the identifier of the client certificate to use for client authentication in an HTTPS (SSL) request.

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

### -param pCertHashBlob [in]

SHA1 hash that identifies the certificate. Use a 20 byte buffer for the hash. For more information, see Remarks.

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
The value for the <i>StoreLocation</i> parameter is not defined in the <a href="/windows/win32/api/bits2_5/ne-bits2_5-bg_cert_store_location">BG_CERT_STORE_LOCATION</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Could not find a store matching the <i>StoreName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A certificate matching the hash was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_NULL_REF_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>StoreName</i> or <i>pCertHashBlob</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_BAD_STUB_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCertHashBlob</i> buffer size is not 20 bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The <i>StoreName</i> parameter is more than 256 characters.

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

If you create a certificate for the job or application, you could store the certificate identifier (thumbprint) in the registry or database and use it when a job requires a certificate. You could also enumerate the certificates in the store and let the user choose the certificate. Another alternative is to call the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>  function to retrieve the certificate context based on some criteria. Using the context, call the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function to retrieve the hash (specify CERT_HASH_PROP_ID for <i>dwPropId</i>).

SmartCard thumbprints are not supported.


#### Examples

The following example shows how to specify a client certificate for a job using the thumbprint of the certificate. The example hard codes the thumbprint of the certificate and assumes pJob points to a valid job. 


```cpp

  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;  
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;
  BYTE Thumbprint[] = {0xa1, 0x06, 0x6e, 0x13, 0xf2, 0x34, 0x49, 0x0a, 0x22, 0xd7, 0x6f, 0xb2, 0x80, 0xab, 0x68, 0x7d, 0x16, 0x55, 0xb3, 0x14};


  // Retrieve a pointer to the IBackgroundCopyJob4 interface.
  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&pHttpOptions);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"QueryInterface for HttpOptions failed with 0x%x.\n", hr);
    goto cleanup;
  }

  // Use the client certificate in the current user's personal (MY) store.
  hr = pHttpOptions->SetClientCertificateByID(BG_CERT_STORE_LOCATION_CURRENT_USER, 
      L"MY", Thumbprint);
  if (FAILED(hr))
  {
    wprintf(L"pHttpOptions->SetClientCertificateByID failed with 0x%x.\n", hr);
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



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>