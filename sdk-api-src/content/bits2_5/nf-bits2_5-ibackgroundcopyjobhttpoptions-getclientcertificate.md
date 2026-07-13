---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.GetClientCertificate
title: IBackgroundCopyJobHttpOptions::GetClientCertificate (bits2_5.h)
description: Retrieves the client certificate from the job.
helpviewer_keywords: ["GetClientCertificate","GetClientCertificate method [BITS]","GetClientCertificate method [BITS]","IBackgroundCopyJobHttpOptions interface","IBackgroundCopyJobHttpOptions interface [BITS]","GetClientCertificate method","IBackgroundCopyJobHttpOptions.GetClientCertificate","IBackgroundCopyJobHttpOptions::GetClientCertificate","bits.ibackgroundcopyjobhttpoptions_getclientcertificate","bits2_5/IBackgroundCopyJobHttpOptions::GetClientCertificate"]
old-location: bits\ibackgroundcopyjobhttpoptions_getclientcertificate.htm
tech.root: Bits
ms.assetid: cd317bf9-1d4b-438e-beec-15ea7da90fc9
ms.date: 12/05/2018
ms.keywords: GetClientCertificate, GetClientCertificate method [BITS], GetClientCertificate method [BITS],IBackgroundCopyJobHttpOptions interface, IBackgroundCopyJobHttpOptions interface [BITS],GetClientCertificate method, IBackgroundCopyJobHttpOptions.GetClientCertificate, IBackgroundCopyJobHttpOptions::GetClientCertificate, bits.ibackgroundcopyjobhttpoptions_getclientcertificate, bits2_5/IBackgroundCopyJobHttpOptions::GetClientCertificate
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
 - IBackgroundCopyJobHttpOptions::GetClientCertificate
 - bits2_5/IBackgroundCopyJobHttpOptions::GetClientCertificate
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
 - IBackgroundCopyJobHttpOptions.GetClientCertificate
---

# IBackgroundCopyJobHttpOptions::GetClientCertificate


## -description

Retrieves the client certificate from the job.

## -parameters

### -param pStoreLocation [out]

Identifies the location of a system store to use for looking up the certificate. For possible values, see the <a href="/windows/win32/api/bits2_5/ne-bits2_5-bg_cert_store_location">BG_CERT_STORE_LOCATION</a> enumeration.

### -param pStoreName [out]

Null-terminated string that contains the name of the certificate store. To free the string when done, call  the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param ppCertHashBlob [out]

SHA1 hash that identifies the certificate. To free the blob when done, call  the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param pSubjectName [out]

Null-terminated string that contains the simple subject name of the certificate. The RDNs in the subject name are in the reverse order from what the certificate displays. Subject name can be empty if the certificate does not contain a subject name. To free the string when done, call  the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
Successfully retrieved the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_BAD_STUB_DATA</b></dt>
</dl>
</td>
<td width="60%">
The job does not specify a certificate or the user does not have permissions to the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_NULL_REF_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You use the <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a> or <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a> method to specify the certificate.


#### Examples

The following example shows how to retrieve information about the client certificate. The example assumes pJob points to a valid job. 


```cpp
#define THUMBPRINT_SIZE 20

  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;
  GUID JobId;

  BG_CERT_STORE_LOCATION StoreLocation;
  LPWSTR pStoreName = NULL;
  BYTE* pThumbprint = NULL;
  LPWSTR pSubjectName = NULL;

  // Retrieve a pointer to the IBackgroundCopyJobHttpOptions interface.
  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&pHttpOptions);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }

  // Retrieve information about the client certificate set on the job. 
  hr = pHttpOptions->GetClientCertificate(&StoreLocation, &pStoreName, 
         &pThumbprint, &pSubjectName);
  if (S_OK == hr)
  {
    wprintf(L"\nLocation: %d\nStore name: %s\nSubject: %s\n", 
        StoreLocation, pStoreName, pSubjectName);

    wprintf(L"Thumbprint: ");
    for (DWORD i = 0; i < THUMBPRINT_SIZE; i++)
    {
      wprintf(L"%x ", pThumbprint[i]);
    }
    wprintf(L"\n");

    CoTaskMemFree(pStoreName);
    CoTaskMemFree(pThumbprint);
    CoTaskMemFree(pSubjectName);
  }
  else if (RPC_X_BAD_STUB_DATA == hr)
  {
    wprintf(L"The job does not specify a client certificate or\n"
            L"the user does not have permission to access the certificate.\n");
  }
  else
  {
    wprintf(L"pHttpOptions->GetClientCertificate failed with 0x%x.\n", hr);
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



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-removeclientcertificate">IBackgroundCopyJobHttpOptions::RemoveClientCertificate</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>