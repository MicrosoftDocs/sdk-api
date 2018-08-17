---
UID: NF:bits.IBackgroundCopyManager.GetErrorDescription
title: IBackgroundCopyManager::GetErrorDescription
author: windows-sdk-content
description: Retrieves a description for the specified error code.
old-location: bits\ibackgroundcopymanager_geterrordescription.htm
old-project: bits
ms.assetid: e62e2bde-485d-42d4-b824-a682ab9e16ca
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [BITS], GetErrorDescription method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],GetErrorDescription method, IBackgroundCopyManager.GetErrorDescription, IBackgroundCopyManager::GetErrorDescription, _drz_ibackgroundcopymanager_geterrordescription, bits.ibackgroundcopymanager_geterrordescription, bits/IBackgroundCopyManager::GetErrorDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyManager.GetErrorDescription
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyManager::GetErrorDescription


## -description


Retrieves a description for the specified error code.


## -parameters




### -param hResult [in]

Error code from a previous call to a BITS method.


### -param LanguageId [in]

Identifies the language identifier to use to generate the description. To create the language identifier, use the 
<a href="https://msdn.microsoft.com/en-us/library/Dd373908(v=VS.85).aspx">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>


### -param pErrorDescription






#### - ppErrorDescription [out]

Null-terminated string that contains a description of the error. Call the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>ppErrorDescription</i> when done.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa363050(v=VS.85).aspx">IBackgroundCopyManager</a> interface pointer. For details on creating the 
<b>IBackgroundCopyManager</b> interface pointer, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa362832(v=VS.85).aspx">Connecting to the BITS Service</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Aa362845(v=VS.85).aspx">Handling Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362875(v=VS.85).aspx">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363025(v=VS.85).aspx">IBackgroundCopyJob::GetError</a>
 

 

