---
UID: NF:bits.IBackgroundCopyManager.GetErrorDescription
title: IBackgroundCopyManager::GetErrorDescription
author: windows-sdk-content
description: Retrieves a description for the specified error code.
old-location: bits\ibackgroundcopymanager_geterrordescription.htm
tech.root: Bits
ms.assetid: e62e2bde-485d-42d4-b824-a682ab9e16ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [BITS], GetErrorDescription method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],GetErrorDescription method, IBackgroundCopyManager.GetErrorDescription, IBackgroundCopyManager::GetErrorDescription, _drz_ibackgroundcopymanager_geterrordescription, bits.ibackgroundcopymanager_geterrordescription, bits/IBackgroundCopyManager::GetErrorDescription
ms.topic: method
req.header: bits.h
req.include-header: 
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
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
req.typenames: 
req.redist: 
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


### -param pErrorDescription [out]

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


```cpp
HRESULT hr = 0;
IBackgroundCopyJob* pJob = NULL;
WCHAR* pszDescription = NULL;

//Call fails because the third parameter is NULL.
hr = g_XferManager->CreateJob(L"DummyJob", BG_JOB_TYPE_DOWNLOAD, NULL, &pJob);
if (FAILED(hr))
{
  hr = g_XferManager->GetErrorDescription(hr, LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    //Do something with pszDescription.
    CoTaskMemFree(pszDescription);
  }
}
```





## -see-also




<a href="https://msdn.microsoft.com/cbc182ce-c853-492e-8953-21c54500875b">Handling Errors</a>



<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a>
 

 

