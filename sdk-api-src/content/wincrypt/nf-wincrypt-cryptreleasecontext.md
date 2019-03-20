---
UID: NF:wincrypt.CryptReleaseContext
title: CryptReleaseContext function (wincrypt.h)
author: windows-sdk-content
description: Releases the handle of a cryptographic service provider (CSP) and a key container.
old-location: security\cryptreleasecontext.htm
tech.root: SecCrypto
ms.assetid: c1e3e708-b543-4e87-8638-a9946a83e614
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptReleaseContext, CryptReleaseContext function [Security], _crypto2_cryptreleasecontext, security.cryptreleasecontext, wincrypt/CryptReleaseContext
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptReleaseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptReleaseContext function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptReleaseContext</b> function releases the handle of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) and a <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a>. At each call to this function, the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the CSP is reduced by one. When the reference count reaches zero, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> is fully released and it can no longer be used by any function in the application.

An application calls this function after finishing the use of the CSP. After this function is called, the released CSP handle is no longer valid. This function does not destroy <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key containers</a> or <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key pairs</a>.


## -parameters




### -param hProv [in]

Handle of a cryptographic service provider (CSP) created by a call to 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>.


### -param dwFlags [in]

Reserved for future use and must be zero. If <i>dwFlags</i> is not set to zero, this function returns <b>FALSE</b> but the CSP is released.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The CSP <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> specified by <i>hProv</i> is currently being used by another <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProv</i> parameter does not contain a valid context handle.

</td>
</tr>
</table>
 




## -remarks



After this function has been called, the CSP session is finished and all existing session keys and <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash objects</a> created by using the <i>hProv</i> handle are no longer valid. In practice, all of these objects should be destroyed with calls to 
<a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> and 
<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a> before <b>CryptReleaseContext</b> is called.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/15d4a05d-5888-4532-91fd-6cd94afe0b99">Example C Program: Creating and Hashing a Session Key</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a>



<a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Service Provider Functions</a>
 

 

