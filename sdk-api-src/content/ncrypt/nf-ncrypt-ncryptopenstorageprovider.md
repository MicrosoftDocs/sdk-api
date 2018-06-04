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

# NCryptOpenStorageProvider function


## -description


The <b>NCryptOpenStorageProvider</b> function loads and initializes a CNG key storage provider.


## -parameters




### -param phProvider [out]

A pointer to a <b>NCRYPT_PROV_HANDLE</b> variable that receives the provider handle. When you have finished using this handle, release it by passing it to the <a href="https://msdn.microsoft.com/a5535cf9-ba8c-4212-badd-f1dc88903624">NCryptFreeObject</a> function.


### -param pszProviderName [in, optional]

A pointer to a null-terminated Unicode string that identifies the key storage provider to load. This is the registered alias of the key storage provider. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default key storage provider is loaded. The following values identify the built-in key storage providers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MS_KEY_STORAGE_PROVIDER"></a><a id="ms_key_storage_provider"></a><dl>
<dt><b>MS_KEY_STORAGE_PROVIDER</b></dt>
<dt>L"Microsoft Software Key Storage Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the software key storage provider that is provided by Microsoft.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_SMART_CARD_KEY_STORAGE_PROVIDER"></a><a id="ms_smart_card_key_storage_provider"></a><dl>
<dt><b>MS_SMART_CARD_KEY_STORAGE_PROVIDER</b></dt>
<dt>L"Microsoft Smart Card Key Storage Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the smart card key storage provider that is provided by Microsoft.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Flags that modify the behavior of the function. No flags are defined for this function.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains one or more flags that are not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



In the case that an error condition is returned, the provider will have been unloaded from memory. Functions within the provider must not be called after a failure error is returned.

A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



