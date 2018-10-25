---
UID: NF:wincrypt.CryptExportKey
title: CryptExportKey function
author: windows-sdk-content
description: Exports a cryptographic key or a key pair from a cryptographic service provider (CSP) in a secure manner.
old-location: security\cryptexportkey.htm
tech.root: seccrypto
ms.assetid: 8a7c7b46-3bea-4043-b568-6d91d6335737
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CRYPT_BLOB_VER3, CRYPT_DESTROYKEY, CRYPT_OAEP, CRYPT_SSL2_FALLBACK, CRYPT_Y_ONLY, CryptExportKey, CryptExportKey function [Security], OPAQUEKEYBLOB, PLAINTEXTKEYBLOB, PRIVATEKEYBLOB, PUBLICKEYBLOB, SIMPLEBLOB, SYMMETRICWRAPKEYBLOB, _crypto2_cryptexportkey, security.cryptexportkey, wincrypt/CryptExportKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
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
 - CryptExportKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptExportKey function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptExportKey</b> function exports a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic key</a> or a key pair from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in a secure manner.

A handle to the key to be exported is passed to the function, and the function returns 
a <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>. This key BLOB can be sent over a nonsecure transport or stored in a nonsecure storage location. This function can export an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Schannel</a> session key, regular <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a>, <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>, or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a>. The key BLOB to export is useless until the intended recipient uses the 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a> function on it to import the key or key pair into a recipient's CSP.


## -parameters




### -param hKey [in]

A handle to the key to be exported.


### -param hExpKey [in]

A handle to a cryptographic key of the destination user. The key data within the exported <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> is encrypted using this key. This ensures that only the destination user is able to make use of the key BLOB.  Both <i>hExpKey</i> and <i>hKey</i> must come from the same CSP.


Most often, this is the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key exchange public key</a> of the destination user. However, certain protocols in some CSPs require that a session key belonging to the destination user be used for this purpose.

If the key BLOB type specified by <i>dwBlobType</i> is <b>PUBLICKEYBLOB</b>, this parameter is unused and must be set to zero.

If the key BLOB type specified by <i>dwBlobType</i> is <b>PRIVATEKEYBLOB</b>, this is typically a handle to a session key that is to be used to encrypt the key BLOB. Some CSPs allow this parameter to be zero, in which case the application must encrypt the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> manually so as to protect it.

To determine how Microsoft <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> respond to this parameter, see the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> sections of 
<a href="https://msdn.microsoft.com/1461914e-5506-4f24-97da-3d2148aafd1c">Microsoft Cryptographic Service Providers</a>.

<div class="alert"><b>Note</b>  Some CSPs may modify this parameter as a result of the operation. Applications that subsequently use this key for other purposes should call the  <a href="https://msdn.microsoft.com/c5658008-7c92-4877-871a-a764884efd79">CryptDuplicateKey</a> function to create a duplicate key handle. When the application has finished using the handle, release it by calling the <a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> function.</div>
<div> </div>

### -param dwBlobType [in]

Specifies the type of <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> to be exported in <i>pbData</i>. This must be one of the following constants as discussed in 
<a href="https://msdn.microsoft.com/859b1bfe-6182-4728-a721-1f34cc98f66f">Cryptographic Key Storage and Exchange</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPAQUEKEYBLOB"></a><a id="opaquekeyblob"></a><dl>
<dt><b>OPAQUEKEYBLOB</b></dt>
</dl>
</td>
<td width="60%">
Used to store session keys in an Schannel CSP or any other vendor-specific format. OPAQUEKEYBLOBs are nontransferable and must be used within the CSP that generated the BLOB.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIVATEKEYBLOB"></a><a id="privatekeyblob"></a><dl>
<dt><b>PRIVATEKEYBLOB</b></dt>
</dl>
</td>
<td width="60%">
Used to transport <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pairs</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PUBLICKEYBLOB"></a><a id="publickeyblob"></a><dl>
<dt><b>PUBLICKEYBLOB</b></dt>
</dl>
</td>
<td width="60%">
Used to transport public keys.

</td>
</tr>
<tr>
<td width="40%"><a id="SIMPLEBLOB"></a><a id="simpleblob"></a><dl>
<dt><b>SIMPLEBLOB</b></dt>
</dl>
</td>
<td width="60%">
Used to transport session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PLAINTEXTKEYBLOB"></a><a id="plaintextkeyblob"></a><dl>
<dt><b>PLAINTEXTKEYBLOB</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/69FE94D0-8FB5-4EFE-BD84-64B439B3ADE8">PLAINTEXTKEYBLOB</a> used to export any key supported by the CSP in use. 

</td>
</tr>
<tr>
<td width="40%"><a id="SYMMETRICWRAPKEYBLOB"></a><a id="symmetricwrapkeyblob"></a><dl>
<dt><b>SYMMETRICWRAPKEYBLOB</b></dt>
</dl>
</td>
<td width="60%">
Used to export and import a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> wrapped with another symmetric key. The actual wrapped key is in the format specified in the IETF <a href="http://go.microsoft.com/fwlink/p/?linkid=84565">RFC 3217</a> standard.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Specifies additional options for the function. This parameter can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_BLOB_VER3"></a><a id="crypt_blob_ver3"></a><dl>
<dt><b>CRYPT_BLOB_VER3</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
This flag causes this function to export version 3 of a BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DESTROYKEY"></a><a id="crypt_destroykey"></a><dl>
<dt><b>CRYPT_DESTROYKEY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This flag destroys the original key in the OPAQUEKEYBLOB. This flag is available in Schannel CSPs only.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OAEP"></a><a id="crypt_oaep"></a><dl>
<dt><b>CRYPT_OAEP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
This flag causes PKCS #1 version 2 formatting to be created with the RSA encryption and decryption when exporting SIMPLEBLOBs.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SSL2_FALLBACK"></a><a id="crypt_ssl2_fallback"></a><dl>
<dt><b>CRYPT_SSL2_FALLBACK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The first eight bytes of the RSA encryption block <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a> must be set to 0x03 rather than to random data. This prevents version rollback attacks and is discussed in the SSL3 specification. This flag is available for Schannel CSPs only.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_Y_ONLY"></a><a id="crypt_y_only"></a><dl>
<dt><b>CRYPT_Y_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>
 


### -param pbData [out]

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> data. The format of this BLOB varies depending on the BLOB type requested in the <i>dwBlobType</i> parameter. For the format for PRIVATEKEYBLOBs, PUBLICKEYBLOBs, and SIMPLEBLOBs, see 
<a href="https://msdn.microsoft.com/b4592036-0fa3-4b7e-beed-78cf1d2f39a9">Base Provider Key BLOBs</a>.

If this parameter is <b>NULL</b>, the required buffer size is placed in the value pointed to by the <i>pdwDataLen</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that, on entry, contains the size, in bytes, of the buffer pointed to by the <i>pbData</i> parameter. When the function returns, this value contains the number of bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>
To retrieve the required size of the <i>pbData</i> buffer, pass <b>NULL</b> for <i>pbData</i>. The required buffer size will be placed in the value pointed to by this parameter.


## -returns



If the function succeeds, the function returns  nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP being used. The following table shows some of the possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbData</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pdwDataLen</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_DATA</b></dt>
</dl>
</td>
<td width="60%">
Either the algorithm that works with the public key to be exported is not supported by this CSP, or an attempt was made to export a session key that was encrypted with something other than one of your public keys.

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
<dt><b>NTE_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
One or both of the keys specified by <i>hKey</i> and <i>hExpKey</i> are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY_STATE</b></dt>
</dl>
</td>
<td width="60%">
You do not have permission to export the key. That is, when the <i>hKey</i> key was created, the CRYPT_EXPORTABLE flag was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_PUBLIC_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> type specified by <i>dwBlobType</i> is PUBLICKEYBLOB, but <i>hExpKey</i> does not contain a public key handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwBlobType</i> parameter specifies an unknown BLOB type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the <i>hKey</i> key was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_KEY</b></dt>
</dl>
</td>
<td width="60%">
A session key is being exported, and the <i>hExpKey</i> parameter does not specify a public key.

</td>
</tr>
</table>
 




## -remarks



For any of the DES key permutations that use a PLAINTEXTKEYBLOB, only the full key size, including parity bit, may be exported. The following key sizes are supported.

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

The following example shows how to export a cryptographic key or a key pair in a more secure manner. This example assumes that a cryptographic context has been acquired and that a public key is available for export. For an example that includes the complete context for using this function, see 
<a href="https://msdn.microsoft.com/72f5d30a-efd5-4bf5-8057-cb73e5aa0514">Example C Program: Signing a Hash and Verifying the Hash Signature</a>. For another example that uses this function, see <a href="https://msdn.microsoft.com/a7f2fdd1-9514-4cda-bae2-2f379dd9a27d">Example C Program: Exporting a Session Key</a>.
				


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

BOOL GetExportedKey(
    HCRYPTKEY hKey, 
    DWORD dwBlobType,
    LPBYTE *ppbKeyBlob, 
    LPDWORD pdwBlobLen)
{
    DWORD dwBlobLength;
    *ppbKeyBlob = NULL;
    *pdwBlobLen = 0;

    // Export the public key. Here the public key is exported to a 
    // PUBLICKEYBLOB. This BLOB can be written to a file and
    // sent to another user.

    if(CryptExportKey(   
        hKey,    
        NULL,    
        dwBlobType,
        0,    
        NULL, 
        &dwBlobLength)) 
    {
        printf("Size of the BLOB for the public key determined. \n");
    }
    else
    {
        printf("Error computing BLOB length.\n");
        return FALSE;
    }

    // Allocate memory for the pbKeyBlob.
    if(*ppbKeyBlob = (LPBYTE)malloc(dwBlobLength)) 
    {
        printf("Memory has been allocated for the BLOB. \n");
    }
    else
    {
        printf("Out of memory. \n");
        return FALSE;
    }

    // Do the actual exporting into the key BLOB.
    if(CryptExportKey(   
        hKey, 
        NULL,    
        dwBlobType,    
        0,    
        *ppbKeyBlob,    
        &dwBlobLength))
    {
        printf("Contents have been written to the BLOB. \n");
        *pdwBlobLen = dwBlobLength;
    }
    else
    {
        printf("Error exporting key.\n");
        free(*ppbKeyBlob);
        *ppbKeyBlob = NULL;

        return FALSE;
    }

    return TRUE;
}
```





## -see-also




<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Key Generation and Exchange Functions</a>
 

 

