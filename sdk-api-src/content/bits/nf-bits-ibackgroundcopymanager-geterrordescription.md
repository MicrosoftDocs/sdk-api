---
UID: NF:bits.IBackgroundCopyManager.GetErrorDescription
title: IBackgroundCopyManager::GetErrorDescription (bits.h)
description: Retrieves a description for the specified error code.
helpviewer_keywords: ["GetErrorDescription","GetErrorDescription method [BITS]","GetErrorDescription method [BITS]","IBackgroundCopyManager interface","IBackgroundCopyManager interface [BITS]","GetErrorDescription method","IBackgroundCopyManager.GetErrorDescription","IBackgroundCopyManager::GetErrorDescription","_drz_ibackgroundcopymanager_geterrordescription","bits.ibackgroundcopymanager_geterrordescription","bits/IBackgroundCopyManager::GetErrorDescription"]
old-location: bits\ibackgroundcopymanager_geterrordescription.htm
tech.root: Bits
ms.assetid: e62e2bde-485d-42d4-b824-a682ab9e16ca
ms.date: 12/05/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [BITS], GetErrorDescription method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],GetErrorDescription method, IBackgroundCopyManager.GetErrorDescription, IBackgroundCopyManager::GetErrorDescription, _drz_ibackgroundcopymanager_geterrordescription, bits.ibackgroundcopymanager_geterrordescription, bits/IBackgroundCopyManager::GetErrorDescription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyManager::GetErrorDescription
 - bits/IBackgroundCopyManager::GetErrorDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyManager.GetErrorDescription
---

# IBackgroundCopyManager::GetErrorDescription


## -description

Retrieves a description for the specified error code.

## -parameters

### -param hResult [in]

Error code from a previous call to a BITS method.

### -param LanguageId [in]

Identifies the language identifier to use to generate the description. To create the language identifier, use the 
<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>

### -param pErrorDescription [out]

Null-terminated string that contains a description of the error. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppErrorDescription</i> when done.

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
<dt><b>S_OK</b></dt>
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
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager">IBackgroundCopyManager</a> interface pointer. For details on creating the 
<b>IBackgroundCopyManager</b> interface pointer, see 
<a href="/windows/desktop/Bits/connecting-to-the-bits-service">Connecting to the BITS Service</a>.


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

<a href="/windows/desktop/Bits/handling-errors">Handling Errors</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a>