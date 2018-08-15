---
UID: NF:wincrypt.CryptImportKey
title: CryptImportKey function
author: windows-sdk-content
description: Transfers a cryptographic key from a key BLOB into a cryptographic service provider (CSP).
old-location: security\cryptimportkey.htm
old-project: seccrypto
ms.assetid: f48b6ec9-e03b-43b0-9f22-120ae93d934c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CRYPT_EXPORTABLE, CRYPT_IPSEC_HMAC_KEY, CRYPT_NO_SALT, CRYPT_OAEP, CRYPT_USER_PROTECTED, CryptImportKey, CryptImportKey function [Security], _crypto2_cryptimportkey, security.cryptimportkey, wincrypt/CryptImportKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
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
 - CryptImportKey
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptImportKey function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptImportKey</b> function transfers a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic key</a> from a <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> into a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This function can be used to import an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Schannel</a> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a>, regular session key, <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>, or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a>. For all but the public key, the key or key pair is encrypted.


## -parameters




### -param hProv [in]

The handle of a CSP obtained with the <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function.


### -param pbData [in]

A <b>BYTE</b> array that contains a 
<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a> BLOB header followed by the encrypted key. This key BLOB is created by the 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> function, either in this application or by another application possibly running on a different computer.


### -param dwDataLen [in]

Contains the length, in bytes, of the key BLOB.


### -param hPubKey [in]

A handle to the cryptographic key that decrypts the key stored in <i>pbData</i>.  This key must come from the same CSP to which <i>hProv</i> refers. The meaning of this parameter differs depending on the CSP type and the type of key BLOB being imported:

<ul>
<li>If the key BLOB is encrypted with the key <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key pair</a>, for example, a <b>SIMPLEBLOB</b>, this parameter can be the handle to the key exchange key.</li>
<li>If the key BLOB is encrypted with a session key, for example, an encrypted <b>PRIVATEKEYBLOB</b>, this parameter contains the handle of this session key.</li>
<li>If the key BLOB is not encrypted, for example, a <b>PUBLICKEYBLOB</b>, this parameter is not used and must be zero.</li>
<li>If the key BLOB is encrypted with a session key in an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Schannel</a> CSP, for example, an encrypted <b>OPAQUEKEYBLOB</b> or any other vendor-specific <b>OPAQUEKEYBLOB</b>, this parameter is not used and must be set to zero.</li>
</ul>
<div class="alert"><b>Note</b>  Some CSPs may modify this parameter as a result of the operation. Applications that subsequently use this key for other purposes should call the  <a href="https://msdn.microsoft.com/c5658008-7c92-4877-871a-a764884efd79">CryptDuplicateKey</a> function to create a duplicate key handle.  When the application has finished using the handle, release it by calling the <a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> function.</div>
<div> </div>

### -param dwFlags [in]

Currently used only when a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a> in the form of a <b>PRIVATEKEYBLOB</b> is imported into the CSP. 



						
					This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
</dl>
</td>
<td width="60%">
The key being imported is eventually to be reexported. If this flag is not used, then calls to 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OAEP"></a><a id="crypt_oaep"></a><dl>
<dt><b>CRYPT_OAEP</b></dt>
</dl>
</td>
<td width="60%">
This flag causes PKCS #1 version 2 formatting to be checked with  RSA encryption and decryption when importing <b>SIMPLEBLOB</b>s.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NO_SALT"></a><a id="crypt_no_salt"></a><dl>
<dt><b>CRYPT_NO_SALT</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">no-salt value</a> gets allocated for a 40-bit <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a>. For more information, see 
<a href="https://msdn.microsoft.com/f1af0af7-c64e-435a-aef0-7c4ed7bd1199">Salt Value Functionality</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the CSP notifies the user through a dialog box or some other method when certain actions are attempted using this key. The precise behavior is specified by the CSP or the CSP type used. 
If the provider context was acquired with CRYPT_SILENT set, using this flag causes a failure and the last error is set to NTE_SILENT_CONTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_IPSEC_HMAC_KEY"></a><a id="crypt_ipsec_hmac_key"></a><dl>
<dt><b>CRYPT_IPSEC_HMAC_KEY</b></dt>
</dl>
</td>
<td width="60%">
Allows for the import of an RC2 key that is larger than 16 bytes. If this flag is not set, calls to the <b>CryptImportKey</b> function with RC2 keys that are greater than 16 bytes fail, and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return <b>NTE_BAD_DATA</b>.

</td>
</tr>
</table>
 


### -param phKey [out]

A pointer to a <b>HCRYPTKEY</b> value that receives the handle of the imported key. When you have finished using the key, release the handle by calling the <a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> function.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Error codes prefaced by "NTE" are generated by the particular CSP being used. Some possible error codes follow.

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
Some CSPs set this error if a private key is imported into a container while another thread or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> is using this key.

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
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">simple key BLOB</a> to be imported is not encrypted with the expected <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key exchange algorithm</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_DATA</b></dt>
</dl>
</td>
<td width="60%">
Either the algorithm that works with the public key to be imported is not supported by this CSP, or an attempt was made to import a session key that was encrypted with something other than one of your public keys.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter specified is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The key BLOB type is not supported by this CSP and is possibly not valid.

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
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_VER</b></dt>
</dl>
</td>
<td width="60%">
The version number of the key BLOB does not match the CSP version. This usually indicates that the CSP needs to be upgraded.

</td>
</tr>
</table>
 




## -remarks



When importing a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">Hash-Based Message Authentication Code</a> (HMAC) key, the caller must identify the imported key as a <b>PLAINTEXTKEYBLOB</b> type and set the appropriate algorithm identifier in the <b>aiKeyAlg</b> field of the <a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a> BLOB header.

The <b>CryptImportKey</b> function can be used to import a plaintext key for symmetric algorithms; however, we recommend that, for ease of use, you use the <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> function instead. When you import a plaintext key, the structure of the key BLOB that is passed in the <i>pbData</i> parameter is a <a href="https://msdn.microsoft.com/69FE94D0-8FB5-4EFE-BD84-64B439B3ADE8">PLAINTEXTKEYBLOB</a>.

You can use the <b>PLAINTEXTKEYBLOB</b> type with any algorithm or type of key combination supported by the CSP in use. 

For an example of importing a plaintext key, see <a href="https://msdn.microsoft.com/23569104-a302-40de-a31a-a4ee22d5f7f2">Example C Program: Importing a Plaintext Key</a>.

The following example shows how you can set the header fields.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>keyBlob.header.bType = PLAINTEXTKEYBLOB;
keyBlob.header.bVersion = CUR_BLOB_VERSION;
keyBlob.header.reserved = 0;
// CALG_AES_128 is used as an example. You would set this to the 
// algorithm id that corresponds to the one used by the key.
keyBlob.header.aiKeyAlg = CALG_AES_128;</pre>
</td>
</tr>
</table></span></div>
The length of the key is specified in keyBlob.keyLength, which is followed by the actual key data.

<div class="alert"><b>Note</b>  The HMAC algorithms do not have their own algorithm identifiers; use CALG_RC2 instead. <b>CRYPT_IPSEC_HMAC_KEY</b> allows the import of RC2 keys longer than 16 bytes.</div>
<div> </div>
For any of the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Data Encryption Standard</a> (DES) key permutations that use <b>PLAINTEXTKEYBLOB</b>, only the full key size, including parity bit, can be imported.

The following key sizes are supported.

<table>
<tr>
<th>Algorithm</th>
<th>Supported key size</th>
</tr>
<tr>
<td>CALG_DES</td>
<td>64 bits</td>
</tr>
<tr>
<td>CALG_3DES_112</td>
<td>128 bits</td>
</tr>
<tr>
<td>CALG_3DES</td>
<td>192 bits</td>
</tr>
</table>
 


#### Examples

The following example shows how to import a key from a key BLOB. For a full example for this function, see 
<a href="https://msdn.microsoft.com/72f5d30a-efd5-4bf5-8057-cb73e5aa0514">Example C Program: Signing a Hash and Verifying the Hash Signature</a>.
For additional code that uses this function, see 
						<a href="https://msdn.microsoft.com/be355b08-95c1-4ad3-bb05-6f646d5db5cd">Example C Program: Decrypting a File</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Wincrypt.h&gt;

BOOL ImportKey(HCRYPTPROV hProv, LPBYTE pbKeyBlob, DWORD dwBlobLen)
{
    HCRYPTKEY hPubKey;

    //---------------------------------------------------------------
    // This code assumes that a cryptographic provider (hProv) 
    // has been acquired and that a key BLOB (pbKeyBlob) that is 
    // dwBlobLen bytes long has been acquired. 

    //---------------------------------------------------------------
    // Get the public key of the user who created the digital 
    // signature and import it into the CSP by using CryptImportKey. 
    // The key to be imported is in the buffer pbKeyBlob that is  
    // dwBlobLen bytes long. This function returns a handle to the 
    // public key in hPubKey.

    if(CryptImportKey(
        hProv,
        pbKeyBlob,
        dwBlobLen,
        0,
        0,
        &amp;hPubKey))
    {
        printf("The key has been imported.\n");
    }
    else
    {
        printf("Public key import failed.\n");
        return FALSE;
    }

    //---------------------------------------------------------------
    // Insert code that uses the imported public key here.
    //---------------------------------------------------------------

    //---------------------------------------------------------------
    // When you have finished using the key, you must release it.
    if(CryptDestroyKey(hPubKey))
    {
        printf("The public key has been released.");
    }
    else
    {
        printf("The public key has not been released.");
        return FALSE;
    }

    return TRUE;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a>



<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Key Generation and Exchange Functions</a>
 

 

