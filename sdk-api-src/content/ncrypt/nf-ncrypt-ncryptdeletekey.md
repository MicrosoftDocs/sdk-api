---
UID: NF:ncrypt.NCryptDeleteKey
title: NCryptDeleteKey function
author: windows-sdk-content
description: Deletes a CNG key.
old-location: security\ncryptdeletekey_func.htm
old-project: seccng
ms.assetid: 2e1958a7-51e0-4731-b4cf-a90d6c1f9ae0
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptDeleteKey, NCryptDeleteKey function [Security], ncrypt/NCryptDeleteKey, security.ncryptdeletekey_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptDeleteKey
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NCryptDeleteKey function


## -description


The <b>NCryptDeleteKey</b> function deletes a CNG key.


## -parameters




### -param hKey [in]

The handle of the key to delete. This handle is obtained by using the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.

<div class="alert"><b>Note</b>  The <b>NCryptDeleteKey</b> function frees the handle. Applications must not use the handle or attempt to call the <a href="https://msdn.microsoft.com/a5535cf9-ba8c-4212-badd-f1dc88903624">NCryptFreeObject</a> function on it after calling the <b>NCryptDeleteKey</b> function.</div>
<div> </div>

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of values that is specific to each key storage provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


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
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.




## -see-also




<a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a>
 

 

