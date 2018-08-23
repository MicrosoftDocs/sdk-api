---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.GetClientCertificate
title: IBackgroundCopyJobHttpOptions::GetClientCertificate
author: windows-sdk-content
description: Retrieves the client certificate from the job.
old-location: bits\ibackgroundcopyjobhttpoptions_getclientcertificate.htm
old-project: bits
ms.assetid: cd317bf9-1d4b-438e-beec-15ea7da90fc9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetClientCertificate, GetClientCertificate method [BITS], GetClientCertificate method [BITS],IBackgroundCopyJobHttpOptions interface, IBackgroundCopyJobHttpOptions interface [BITS],GetClientCertificate method, IBackgroundCopyJobHttpOptions.GetClientCertificate, IBackgroundCopyJobHttpOptions::GetClientCertificate, bits.ibackgroundcopyjobhttpoptions_getclientcertificate, bits2_5/IBackgroundCopyJobHttpOptions::GetClientCertificate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits2_5.h
req.include-header: Bits.h
req.redist: 
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
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
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyJobHttpOptions::GetClientCertificate


## -description


Retrieves the client certificate from the job.


## -parameters




### -param pStoreLocation [out]

Identifies the location of a system store to use for looking up the certificate. For possible values, see the <a href="https://msdn.microsoft.com/596b1ba1-6652-4c97-a44d-e8271471d864">BG_CERT_STORE_LOCATION</a> enumeration.


### -param pStoreName [out]

Null-terminated string that contains the name of the certificate store. To free the string when done, call  the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param ppCertHashBlob [out]

SHA1 hash that identifies the certificate. To free the blob when done, call  the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param pSubjectName [out]

Null-terminated string that contains the simple subject name of the certificate. The RDNs in the subject name are in the reverse order from what the certificate displays. Subject name can be empty if the certificate does not contain a subject name. To free the string when done, call  the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>RPC_X_BAD_STUB_DATA</b></b></dt>
</dl>
</td>
<td width="60%">
The job does not specify a certificate or the user does not have permissions to the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>RPC_X_NULL_REF_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You use the <a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a> or <a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a> method to specify the certificate.


#### Examples

The following example shows how to retrieve information about the client certificate. The example assumes pJob points to a valid job. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define THUMBPRINT_SIZE 20

  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;
  GUID JobId;

  BG_CERT_STORE_LOCATION StoreLocation;
  LPWSTR pStoreName = NULL;
  BYTE* pThumbprint = NULL;
  LPWSTR pSubjectName = NULL;

  // Retrieve a pointer to the IBackgroundCopyJobHttpOptions interface.
  hr = pJob-&gt;QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&amp;pHttpOptions);
  pJob-&gt;Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob-&gt;QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }

  // Retrieve information about the client certificate set on the job. 
  hr = pHttpOptions-&gt;GetClientCertificate(&amp;StoreLocation, &amp;pStoreName, 
         &amp;pThumbprint, &amp;pSubjectName);
  if (S_OK == hr)
  {
    wprintf(L"\nLocation: %d\nStore name: %s\nSubject: %s\n", 
        StoreLocation, pStoreName, pSubjectName);

    wprintf(L"Thumbprint: ");
    for (DWORD i = 0; i &lt; THUMBPRINT_SIZE; i++)
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
    wprintf(L"pHttpOptions-&gt;GetClientCertificate failed with 0x%x.\n", hr);
    goto cleanup;
  }


cleanup:

  if (pHttpOptions)
  {
    hr = pHttpOptions-&gt;Release();
  }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d8ccf65d-a4f1-44d9-9903-43e5529f1f29">IBackgroundCopyJobHttpOptions</a>



<a href="https://msdn.microsoft.com/b4fb7213-5f6b-407f-bc44-6d11886ed5ad">IBackgroundCopyJobHttpOptions::RemoveClientCertificate</a>



<a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>



<a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>
 

 

