---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBackgroundCopyManager::GetErrorDescription


## -description


Retrieves a description for the specified error code.


## -parameters




### -param hResult [in]

Error code from a previous call to a BITS method.


### -param LanguageId [in]

Identifies the language identifier to use to generate the description. To create the language identifier, use the 
<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>


### -param pErrorDescription






#### - ppErrorDescription [out]

Null-terminated string that contains a description of the error. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppErrorDescription</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

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
Error code description was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_RESOURCE_LANG_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No string is available for the locale.

</td>
</tr>
</table>
 




## -remarks



Descriptions for HTTP errors are  localized.

<b>Windows XP/2000:  </b>Descriptions for HTTP errors are not localized.


#### Examples

The following example shows how to retrieve the description associated with an error code. The g_XferManager variable in the example is an 
<a href="https://msdn.microsoft.com/fc98dfb3-7e10-421d-b722-223bd8a65330">IBackgroundCopyManager</a> interface pointer. For details on creating the 
<b>IBackgroundCopyManager</b> interface pointer, see 
<a href="https://msdn.microsoft.com/2fa88277-c7a1-4f1c-a63c-e2d27a163249">Connecting to the BITS Service</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = 0;
IBackgroundCopyJob* pJob = NULL;
WCHAR* pszDescription = NULL;

//Call fails because the third parameter is NULL.
hr = g_XferManager-&gt;CreateJob(L"DummyJob", BG_JOB_TYPE_DOWNLOAD, NULL, &amp;pJob);
if (FAILED(hr))
{
  hr = g_XferManager-&gt;GetErrorDescription(hr, LANGIDFROMLCID(GetThreadLocale()), &amp;pszDescription);
  if (SUCCEEDED(hr))
  {
    //Do something with pszDescription.
    CoTaskMemFree(pszDescription);
  }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cbc182ce-c853-492e-8953-21c54500875b">Handling Errors</a>



<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a>
 

 

