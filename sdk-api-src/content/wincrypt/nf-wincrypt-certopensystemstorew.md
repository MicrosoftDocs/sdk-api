---
UID: NF:wincrypt.CertOpenSystemStoreW
title: CertOpenSystemStoreW function (wincrypt.h)
author: windows-sdk-content
description: Opens the most common system certificate store. To open certificate stores with more complex requirements, such as file-based or memory-based stores, use CertOpenStore.
old-location: security\certopensystemstore.htm
tech.root: SecCrypto
ms.assetid: 23699439-1a6c-4907-93fa-651024856be7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CA, CertOpenSystemStore, CertOpenSystemStore function [Security], CertOpenSystemStoreA, CertOpenSystemStoreW, MY, ROOT, SPC, _crypto2_certopensystemstore, security.certopensystemstore, wincrypt/CertOpenSystemStore, wincrypt/CertOpenSystemStoreA, wincrypt/CertOpenSystemStoreW
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertOpenSystemStoreW (Unicode) and CertOpenSystemStoreA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertOpenSystemStore
 - CertOpenSystemStoreA
 - CertOpenSystemStoreW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertOpenSystemStoreW function


## -description


The <b>CertOpenSystemStore</b> function is a simplified function that opens the most common system <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. To open certificate stores with more complex requirements, such as file-based or memory-based stores, use <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>.


## -parameters




### -param hProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). Set <i>hProv</i> to <b>NULL</b> to use the default CSP. If <i>hProv</i> is not <b>NULL</b>, it must be a CSP handle created by using the <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function.This parameter's data type is <b>HCRYPTPROV</b>.




### -param szSubsystemProtocol [in]

A string that names a system store. If the system store name provided in this parameter is not the name of an existing system store, a new system store will be created and used. <a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a> can be used to list the names of existing system stores. Some example system stores are listed in the following table.

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
<a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certification authority</a> certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="MY"></a><a id="my"></a><dl>
<dt><b>MY</b></dt>
</dl>
</td>
<td width="60%">
A certificate store that holds certificates with associated private keys.

</td>
</tr>
<tr>
<td width="40%"><a id="ROOT"></a><a id="root"></a><dl>
<dt><b>ROOT</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">Root certificates</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPC"></a><a id="spc"></a><dl>
<dt><b>SPC</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Software Publisher Certificate</a>.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns a handle to the certificate store.

If the function fails, it returns <b>NULL</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called function <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> are propagated to this function.</div>
<div> </div>



## -remarks



Only current user certificates are accessible using this method, not the local machine store.

After the system store is opened, all the standard certificate store functions can be used to manipulate the certificates.

After use, the store should be closed by using <a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a>.

For more information about the stores that are automatically migrated, see <a href="https://msdn.microsoft.com/fe81d578-f2f6-41f0-9ebf-e7bd5532bed9">Certificate Store Migration</a>.


#### Examples

The following example shows a simplified method for opening the most common system certificate stores. For another example that uses this function, see <a href="https://msdn.microsoft.com/cf87791c-b98c-4dd7-b346-336c4b1a88ca">Example C Program: Certificate Store Operations</a>.


```cpp
//--------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE  hSystemStore;              // system store handle

//--------------------------------------------------------------------
// Open the CA system certificate store. The same call can be
// used with the name of a different system store, such as My or Root,
// as the second parameter.

if(hSystemStore = CertOpenSystemStore(
    0,
    "CA"))
{
  printf("The CA system store is open. Continue.\n");
}
else
{
  printf("The CA system store did not open.\n");
  exit(1);
}

// Use the store as needed.
// ...

// When done using the store, close it.
if(!CertCloseStore(hSystemStore, 0))
{
  printf("Unable to close the CA system store.\n");
  exit(1);
}
```





## -see-also




<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a>



<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a>



<a href="https://msdn.microsoft.com/16c2cc06-28fd-42d9-a377-0df2eaeeae56">CertGetCRLContextProperty</a>



<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>



<a href="https://msdn.microsoft.com/5cc818d7-b079-4962-aabc-fc512d4e92ac">CertSaveStore</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Store Functions</a>
 

 

