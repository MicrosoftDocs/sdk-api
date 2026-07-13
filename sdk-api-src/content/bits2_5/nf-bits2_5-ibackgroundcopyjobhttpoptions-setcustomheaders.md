---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.SetCustomHeaders
title: IBackgroundCopyJobHttpOptions::SetCustomHeaders (bits2_5.h)
description: Specifies one or more custom HTTP headers to include in HTTP requests.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions interface [BITS]","SetCustomHeaders method","IBackgroundCopyJobHttpOptions.SetCustomHeaders","IBackgroundCopyJobHttpOptions::SetCustomHeaders","SetCustomHeaders","SetCustomHeaders method [BITS]","SetCustomHeaders method [BITS]","IBackgroundCopyJobHttpOptions interface","bits.ibackgroundcopyjobhttpoptions_setcustomheaders","bits2_5/IBackgroundCopyJobHttpOptions::SetCustomHeaders"]
old-location: bits\ibackgroundcopyjobhttpoptions_setcustomheaders.htm
tech.root: Bits
ms.assetid: 422a331d-5b6b-48ec-b040-43a88be43ac3
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJobHttpOptions interface [BITS],SetCustomHeaders method, IBackgroundCopyJobHttpOptions.SetCustomHeaders, IBackgroundCopyJobHttpOptions::SetCustomHeaders, SetCustomHeaders, SetCustomHeaders method [BITS], SetCustomHeaders method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_setcustomheaders, bits2_5/IBackgroundCopyJobHttpOptions::SetCustomHeaders
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
 - IBackgroundCopyJobHttpOptions::SetCustomHeaders
 - bits2_5/IBackgroundCopyJobHttpOptions::SetCustomHeaders
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
 - IBackgroundCopyJobHttpOptions.SetCustomHeaders
---

# IBackgroundCopyJobHttpOptions::SetCustomHeaders


## -description

Specifies one or more custom HTTP headers to include in HTTP requests.

## -parameters

### -param RequestHeaders [in]

Null-terminated string that contains the custom headers to append to the HTTP request. Each header must be terminated by a carriage return and line feed (CR/LF) character. The string is limited to 16,384 characters, including the null terminator.

To remove the custom headers from the job, set the <i>RequestHeaders</i> parameter to <b>NULL</b>.

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
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The length of the custom headers is more than 16 KB.

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

The custom headers are applicable only to remote files that use the HTTP or HTTPS protocol. You can specify custom headers for all job types.

Only the job owner can specify custom headers. If the job changes ownership, BITS removes the headers from the job.

Note that if multiple HTTP requests are sent, the headers are sent with each request.

An ISAPI that processes the custom header can return an HTTP error if the header is not valid. For details on how BITS handles the error, see <a href="/windows/desktop/Bits/handling-server-application-errors">Handling Server Application Errors</a>.


#### Examples

The following example shows how to specify custom headers for a job. The example assumes that pJob points to a valid job.


```cpp
// Custom headers to include in job.
#define HEADERS L"MyHeader_1: Header One Value\r\n" \
    L"MyHeader_2: Header Two Value\r\n" \
    L"MyHeader_3: Header Three Value\r\n"


  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&pHttpOptions);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }

  hr = pHttpOptions->SetCustomHeaders(HEADERS);
  if (FAILED(hr))
  {
    wprintf(L"pHttpOptions->SetCustomHeaders failed with 0x%x.\n", hr);
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



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getcustomheaders">IBackgroundCopyJobHttpOptions::GetCustomHeaders</a>