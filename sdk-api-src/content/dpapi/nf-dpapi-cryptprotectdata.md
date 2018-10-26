---
UID: NF:dpapi.CryptProtectData
title: CryptProtectData function
author: windows-sdk-content
description: Performs encryption on the data in a DATA_BLOB structure.
old-location: security\cryptprotectdata.htm
tech.root: seccrypto
ms.assetid: 765a68fd-f105-49fc-a738-4a8129eb0770
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CRYPTPROTECT_AUDIT, CRYPTPROTECT_LOCAL_MACHINE, CRYPTPROTECT_UI_FORBIDDEN, CryptProtectData, CryptProtectData function [Security], _crypto2_cryptprotectdata, dpapi/CryptProtectData, security.cryptprotectdata, wincrypt/CryptProtectData
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
 - CryptProtectData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptProtectData function


## -description


The <b>CryptProtectData</b> function performs encryption on the data in a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure. Typically, only a user with the same logon credential as the user who encrypted the data can decrypt the data. In addition, the encryption and decryption usually must be done on the same computer. For information about exceptions, see  Remarks.


## -parameters




### -param pDataIn [in]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a> to be encrypted.


### -param szDataDescr [in, optional]

A string with a readable description of the data to be encrypted. This description string is included with the encrypted data. This parameter is optional and can be set to <b>NULL</b>.


### -param pOptionalEntropy [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure that contains a password or other additional entropy used to encrypt the data. The <b>DATA_BLOB</b> structure used in the encryption phase must also be used in the decryption phase. This parameter can be set to <b>NULL</b> for no additional entropy. For information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param pvReserved [in]

Reserved for future use and must be set to <b>NULL</b>.


### -param pPromptStruct [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/412ce598-a7c9-446d-bd98-6583a20d6cd7">CRYPTPROTECT_PROMPTSTRUCT</a> structure that provides information about where and when prompts are to be displayed and what the content of those prompts should be. This parameter can be set to <b>NULL</b> in both the encryption and decryption phases.


### -param dwFlags [in]

This parameter can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_LOCAL_MACHINE"></a><a id="cryptprotect_local_machine"></a><dl>
<dt><b>CRYPTPROTECT_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, it associates the data encrypted with the current computer instead of with an individual user. Any user on the computer on which <b>CryptProtectData</b> is called can use 
<a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> to decrypt the data.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_UI_FORBIDDEN"></a><a id="cryptprotect_ui_forbidden"></a><dl>
<dt><b>CRYPTPROTECT_UI_FORBIDDEN</b></dt>
</dl>
</td>
<td width="60%">
This flag is used for remote situations where presenting a user interface (UI) is not an option. When this flag is set and a UI is specified for either the protect or unprotect operation, the operation fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the ERROR_PASSWORD_RESTRICTION code.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_AUDIT"></a><a id="cryptprotect_audit"></a><dl>
<dt><b>CRYPTPROTECT_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
This flag generates an audit on protect and unprotect operations.

</td>
</tr>
</table>
 


### -param pDataOut [out]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure that receives the encrypted data. When you have finished using the <b>DATA_BLOB</b> structure, free its <b>pbData</b> member by calling the   <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.
						

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Typically, only a user with logon <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> that match those of the user who encrypted the data can decrypt the data. In addition, decryption usually can only be done on the computer where the data was encrypted. However, a user with a roaming profile can decrypt the data from another computer on the network.

If the CRYPTPROTECT_LOCAL_MACHINE flag is set when the data is encrypted, any user on the computer where the encryption was done can decrypt the data.

The function creates a session key to perform the encryption. The session key is derived again when the data is to be decrypted.

The function also adds a <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) (keyed integrity check) to the encrypted data to guard against data tampering.

To encrypt memory for temporary use in the same process or across processes, call the <a href="https://msdn.microsoft.com/6b372552-87d4-4047-afa5-0d1113348289">CryptProtectMemory</a> function.


#### Examples

The following example shows encryption of the data in a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure. The <b>CryptProtectData</b> function does the encryption by using a session key that the function creates by using the user's logon credentials. For another example that uses this function, see 
<a href="https://msdn.microsoft.com/51607aad-9fa8-4db6-bd2a-3821dce619e7">Example C Program: Using CryptProtectData</a>.


```cpp
// Encrypt data from DATA_BLOB DataIn to DATA_BLOB DataOut.

//--------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataIn;
DATA_BLOB DataOut;
BYTE *pbDataInput =(BYTE *)"Hello world of data protection.";
DWORD cbDataInput = strlen((char *)pbDataInput)+1;

//--------------------------------------------------------------------
// Initialize the DataIn structure.

DataIn.pbData = pbDataInput;    
DataIn.cbData = cbDataInput;

//--------------------------------------------------------------------
//  Begin protect phase. Note that the encryption key is created
//  by the function and is not passed.

if(CryptProtectData(
     &DataIn,
     L"This is the description string.", // A description string
                                         // to be included with the
                                         // encrypted data. 
     NULL,                               // Optional entropy not used.
     NULL,                               // Reserved.
     NULL,                               // Pass NULL for the 
                                         // prompt structure.
     0,
     &DataOut))
{
     printf("The encryption phase worked.\n");
}
else
{
    printf("Encryption error using CryptProtectData.\n");
    exit(1); 
}
```





## -see-also




<a href="https://msdn.microsoft.com/6b372552-87d4-4047-afa5-0d1113348289">CryptProtectMemory</a>



<a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a>



<a href="cryptography_functions.htm">Data Encryption and Decryption Functions</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>
 

 

