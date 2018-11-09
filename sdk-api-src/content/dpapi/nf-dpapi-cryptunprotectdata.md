---
UID: NF:dpapi.CryptUnprotectData
title: CryptUnprotectData function
author: windows-sdk-content
description: Decrypts and does an integrity check of the data in a DATA_BLOB structure.
old-location: security\cryptunprotectdata.htm
tech.root: seccrypto
ms.assetid: 54eab3b0-d341-47c6-9c32-79328d7a7155
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CRYPTPROTECT_UI_FORBIDDEN, CRYPTPROTECT_VERIFY_PROTECTION, CryptUnprotectData, CryptUnprotectData function [Security], _crypto2_cryptunprotectdata, dpapi/CryptUnprotectData, security.cryptunprotectdata, wincrypt/CryptUnprotectData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dpapi.h
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
 - CryptUnprotectData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptUnprotectData function


## -description


The <b>CryptUnprotectData</b> function decrypts and does an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> check of the data in a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure. Usually, the only user who can decrypt the data is a user with the same logon <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> as the user who encrypted the data. In addition, the encryption and decryption must be done on the same computer. For information about exceptions, see the Remarks section of 
<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a>.


## -parameters




### -param pDataIn [in]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure that holds the encrypted data. The <b>DATA_BLOB</b> structure's <b>cbData</b> member holds the length of the <b>pbData</b> member's byte string that contains the text to be encrypted.


### -param ppszDataDescr [out, optional]

A pointer to a string-readable description of the encrypted data included with the encrypted data. This parameter can be set to <b>NULL</b>.  When you have finished using <i>ppszDataDescr</i>, free it by calling the  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


### -param pOptionalEntropy [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure that contains a password or other additional entropy used when the data was encrypted. This parameter can be set to <b>NULL</b>; however, if an optional entropy <b>DATA_BLOB</b> structure was used in the encryption phase, that same <b>DATA_BLOB</b> structure must be used for the decryption phase. For information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param pvReserved

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param pPromptStruct [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/412ce598-a7c9-446d-bd98-6583a20d6cd7">CRYPTPROTECT_PROMPTSTRUCT</a> structure that provides information about where and when prompts are to be displayed and what the content of those prompts should be. This parameter can be set to <b>NULL</b>.


### -param dwFlags [in]

A <b>DWORD</b> value that specifies options for this function. This parameter can be zero, in which case no option is set, or the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_UI_FORBIDDEN"></a><a id="cryptprotect_ui_forbidden"></a><dl>
<dt><b>CRYPTPROTECT_UI_FORBIDDEN</b></dt>
</dl>
</td>
<td width="60%">
This flag is used for remote situations where the user interface (UI) is not an option. When this flag is set and UI is specified for either the protect or unprotect operation, the operation fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the ERROR_PASSWORD_RESTRICTION code.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_VERIFY_PROTECTION"></a><a id="cryptprotect_verify_protection"></a><dl>
<dt><b>CRYPTPROTECT_VERIFY_PROTECTION</b></dt>
</dl>
</td>
<td width="60%">
This flag verifies the protection of a protected <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>. If the default protection level configured of the host is higher than the current protection level for the BLOB, the function returns <b>CRYPT_I_NEW_PROTECTION_REQUIRED</b> to advise the caller to again protect the plaintext contained in the BLOB.

</td>
</tr>
</table>
 


### -param pDataOut [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure where the function stores the decrypted data. When you have finished using the <b>DATA_BLOB</b> structure, free its <b>pbData</b> member by calling the  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



If the function succeeds, the function returns  <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>.




## -remarks



The 
<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> function creates a session key when the data is encrypted. That key is derived again and used to decrypt the data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.

The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> added to the encrypted data can be used to determine whether the encrypted data was altered in any way. Any tampering results in the return of the ERROR_INVALID_DATA code.

When you have finished using the <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure, free its <b>pbData</b> member by calling the  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function. Any <i>ppszDataDescr</i> that is not <b>NULL</b> must also be freed by using <b>LocalFree</b>.

 When you have finished using sensitive information, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function.  


#### Examples

The following example shows decrypting encrypted data in a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure. This function does the decryption by using a session key that the function creates by using the user's logon credentials. For another example that uses this function, see 
<a href="https://msdn.microsoft.com/51607aad-9fa8-4db6-bd2a-3821dce619e7">Example C Program: Using CryptProtectData</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Decrypt data from DATA_BLOB DataOut to DATA_BLOB DataVerify.

//--------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataOut;
DATA_BLOB DataVerify;
LPWSTR pDescrOut =  NULL;
//--------------------------------------------------------------------
// The buffer DataOut would be created using the CryptProtectData
// function. If may have been read in from a file.

//--------------------------------------------------------------------
//   Begin unprotect phase.

if (CryptUnprotectData(
        &amp;DataOut,
        &amp;pDescrOut,
        NULL,                 // Optional entropy
        NULL,                 // Reserved
        NULL,                 // Here, the optional 
                              // prompt structure is not
                              // used.
        0,
        &amp;DataVerify))
{
     printf("The decrypted data is: %s\n", DataVerify.pbData);
     printf("The description of the data was: %s\n",pDescrOut);
}
else
{
    printf("Decryption error!");
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a>



<a href="https://msdn.microsoft.com/1c7980ac-4e9e-43fd-b6d7-c0d0a69c8040">CryptUnprotectMemory</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Encryption and Decryption Functions</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft Base Cryptographic Provider</a>
 

 

