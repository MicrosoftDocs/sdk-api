---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.SetCustomHeaders
title: IBackgroundCopyJobHttpOptions::SetCustomHeaders
author: windows-sdk-content
description: Specifies one or more custom HTTP headers to include in HTTP requests.
old-location: bits\ibackgroundcopyjobhttpoptions_setcustomheaders.htm
tech.root: Bits
ms.assetid: 422a331d-5b6b-48ec-b040-43a88be43ac3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyJobHttpOptions interface [BITS],SetCustomHeaders method, IBackgroundCopyJobHttpOptions.SetCustomHeaders, IBackgroundCopyJobHttpOptions::SetCustomHeaders, SetCustomHeaders, SetCustomHeaders method [BITS], SetCustomHeaders method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_setcustomheaders, bits2_5/IBackgroundCopyJobHttpOptions::SetCustomHeaders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bits2_5.h
: 
- IBackgroundCopyJobHttpOptions.SetCustomHeaders
: 
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
<dt><b><b>S_OK</b></b></dt>
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

An ISAPI that processes the custom header can return an HTTP error if the header is not valid. For details on how BITS handles the error, see <a href="https://msdn.microsoft.com/en-us/library/Bb525047(v=VS.85).aspx">Handling Server Application Errors</a>.


#### Examples

The following example shows how to specify custom headers for a job. The example assumes that pJob points to a valid job.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Custom headers to include in job.
#define HEADERS L"MyHeader_1: Header One Value\n" \
    L"MyHeader_2: Header Two Value\n" \
    L"MyHeader_3: Header Three Value\n"


  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJobHttpOptions* pHttpOptions = NULL;

  hr = pJob-&gt;QueryInterface(__uuidof(IBackgroundCopyJobHttpOptions), (void**)&amp;pHttpOptions);
  pJob-&gt;Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob-&gt;QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }

  hr = pHttpOptions-&gt;SetCustomHeaders(HEADERS);
  if (FAILED(hr))
  {
    wprintf(L"pHttpOptions-&gt;SetCustomHeaders failed with 0x%x.\n", hr);
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




<a href="https://msdn.microsoft.com/en-us/library/Aa964250(v=VS.85).aspx">IBackgroundCopyJobHttpOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964252(v=VS.85).aspx">IBackgroundCopyJobHttpOptions::GetCustomHeaders</a>
 

 

