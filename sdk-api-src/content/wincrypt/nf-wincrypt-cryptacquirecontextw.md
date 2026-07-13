---
UID: NF:wincrypt.CryptAcquireContextW
title: CryptAcquireContextW function (wincrypt.h)
description: Used to acquire a handle to a particular key container within a particular cryptographic service provider (CSP). This returned handle is used in calls to CryptoAPI functions that use the selected CSP. (Unicode)
helpviewer_keywords: ["CRYPT_DEFAULT_CONTAINER_OPTIONAL", "CRYPT_DELETEKEYSET", "CRYPT_MACHINE_KEYSET", "CRYPT_NEWKEYSET", "CRYPT_SILENT", "CRYPT_VERIFYCONTEXT", "CryptAcquireContext", "CryptAcquireContext function [Security]", "CryptAcquireContextW", "_crypto2_cryptacquirecontext", "security.cryptacquirecontext", "wincrypt/CryptAcquireContext", "wincrypt/CryptAcquireContextW"]
old-location: security\cryptacquirecontext.htm
tech.root: security
ms.assetid: 57e13662-3189-4f8d-b90a-d1fbdc09b63c
ms.date: 12/05/2018
ms.keywords: CRYPT_DEFAULT_CONTAINER_OPTIONAL, CRYPT_DELETEKEYSET, CRYPT_MACHINE_KEYSET, CRYPT_NEWKEYSET, CRYPT_SILENT, CRYPT_VERIFYCONTEXT, CryptAcquireContext, CryptAcquireContext function [Security], CryptAcquireContextA, CryptAcquireContextW, _crypto2_cryptacquirecontext, security.cryptacquirecontext, wincrypt/CryptAcquireContext, wincrypt/CryptAcquireContextA, wincrypt/CryptAcquireContextW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptAcquireContextW (Unicode) and CryptAcquireContextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptAcquireContextW
 - wincrypt/CryptAcquireContextW
dev_langs:
 - c++
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
 - CryptAcquireContext
 - CryptAcquireContextA
 - CryptAcquireContextW
---

# CryptAcquireContextW function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptAcquireContext</b> function is used to acquire a handle to a particular <a href="/windows/desktop/SecGloss/k-gly">key container</a> within a particular <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This returned handle is used in calls to <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a> functions that use the selected CSP.

This function first attempts to find a CSP with the characteristics described in the <i>dwProvType</i> and <i>pszProvider</i> parameters. If the CSP is found, the function attempts to find a key container within the CSP that matches the name specified by the <i>pszContainer</i> parameter. To acquire the <a href="/windows/desktop/SecGloss/c-gly">context</a> and the key container of a <a href="/windows/desktop/SecGloss/p-gly">private key</a> associated with the <a href="/windows/desktop/SecGloss/p-gly">public key</a> of a certificate, use 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey">CryptAcquireCertificatePrivateKey</a>.

With the appropriate setting of <i>dwFlags</i>, this function can also create and destroy key containers and can provide access to a CSP with a temporary key container if access to a private key is not required.

## -parameters

### -param phProv [out]

A pointer to a handle of a CSP. When you have finished using the CSP, release the handle by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a> function.

### -param szContainer [in]

The key container name. This is a null-terminated string that identifies the key container to the CSP. This name is independent of the method used to store the keys. Some CSPs store their key containers internally (in hardware), some use the system registry, and others use the file system. In most cases, when <i>dwFlags</i> is set to CRYPT_VERIFYCONTEXT, <i>pszContainer</i> must be set to <b>NULL</b>. However, for hardware-based CSPs, such as a smart card CSP, can be access publicly available information in the specfied container.

For more information about the usage of the <i>pszContainer</i> parameter, see Remarks.

### -param szProvider [in]

A null-terminated string that contains the name of the CSP to be used. 




If this parameter is <b>NULL</b>, the user default provider is used. For more information, see 
<a href="/windows/desktop/SecCrypto/cryptographic-service-provider-contexts">Cryptographic Service Provider Contexts</a>. For a list of available cryptographic providers, see 
<a href="/windows/desktop/SecCrypto/cryptographic-provider-names">Cryptographic Provider Names</a>.

An application can obtain the name of the CSP in use by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function to read the PP_NAME CSP value in the <i>dwParam</i> parameter.

The default CSP can change between operating system releases. To ensure interoperability on different operating system platforms, the CSP should be explicitly set by using this parameter instead of using the default CSP.

### -param dwProvType [in]

Specifies the type of provider to acquire. Defined provider types are discussed in 
<a href="/windows/desktop/SecCrypto/cryptographic-provider-types">Cryptographic Provider Types</a>.

### -param dwFlags [in]

One or more of the following flags. Note, most applications should set the **CRYPT_VERIFYCONTEXT** flag unless they need to create digital signatures or decrypt messages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFYCONTEXT"></a><a id="crypt_verifycontext"></a><dl>
<dt><b>CRYPT_VERIFYCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The caller does not need access to persisted private keys. Apps that use ephemeral keys, or that perform only <a href="/windows/desktop/SecGloss/h-gly">hashing</a>, <a href="/windows/desktop/SecGloss/e-gly">encryption</a>, and <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> verification should set this flag. Only applications that create signatures or decrypt messages need access to a <a href="/windows/desktop/SecGloss/p-gly">private key</a> (and should not set this flag). 

For file-based CSPs, when this flag is set, the <i>pszContainer</i> parameter must be set to <b>NULL</b>. The application has no access to the persisted private keys of public/private key pairs. When this flag is set, temporary <a href="/windows/desktop/SecGloss/p-gly">public/private key pairs</a> can be created, but they are not persisted.

For hardware-based CSPs, such as a smart card CSP, if the <i>pszContainer</i> parameter is <b>NULL</b> or blank, this flag implies that no access to any keys is required, and that no UI should be presented to the user.  This form is used to connect to the CSP to query its capabilities but not to actually use its keys.
If the <i>pszContainer</i> parameter is not <b>NULL</b> and not blank, then this flag implies that access to only the publicly available information within the specified container is required.  The CSP should not ask for a PIN.  Attempts to access private information (for example, the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a> function) will fail.

When <b>CryptAcquireContext</b> is called, many CSPs require input from the owning user before granting access to the private keys in the <a href="/windows/desktop/SecGloss/k-gly">key container</a>. For example, the private keys can be encrypted, requiring a password from the user before they can be used. However, if the <b>CRYPT_VERIFYCONTEXT</b> flag is specified, access to the private keys is not required and the user interface can be bypassed.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NEWKEYSET"></a><a id="crypt_newkeyset"></a><dl>
<dt><b>CRYPT_NEWKEYSET</b></dt>
</dl>
</td>
<td width="60%">
Creates a new key container with the name specified by <i>pszContainer</i>. If <i>pszContainer</i> is <b>NULL</b>, a key container with the default name is created.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_KEYSET"></a><a id="crypt_machine_keyset"></a><dl>
<dt><b>CRYPT_MACHINE_KEYSET</b></dt>
</dl>
</td>
<td width="60%">
By default, keys and key containers are stored as user keys. For Base Providers, this means that user key containers are stored in the user's profile. A key container created without this flag by an administrator can be accessed only by the user creating the key container and a user with administration privileges.


<b>Windows XP:  </b>A key container created without this flag by an administrator can be accessed only by the user creating the key container and the local system account.



A key container created without this flag by a user that is not an administrator can be accessed only by the user creating the key container and the local system account.

The CRYPT_MACHINE_KEYSET flag can be combined with all of the other flags to indicate that the key container of interest is a computer key container and the CSP treats it as such. For Base Providers, this means that the keys are stored locally on the computer that created the key container. If a key container is to be a computer container, the CRYPT_MACHINE_KEYSET flag must be used with all calls to <b>CryptAcquireContext</b> that reference the computer container. The key container created with CRYPT_MACHINE_KEYSET by an administrator can be accessed only by its creator and by a user with administrator <a href="/windows/desktop/SecGloss/p-gly">privileges</a> unless access rights to the container are granted using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>.


<b>Windows XP:  </b>The key container created with CRYPT_MACHINE_KEYSET by an administrator can be accessed only by its creator and by the local system account unless access rights to the container are granted using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>.



The key container created with CRYPT_MACHINE_KEYSET by a user that is not an administrator can be accessed only by its creator and by the local system account unless access rights to the container are granted using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>.

The CRYPT_MACHINE_KEYSET flag is useful when the user is accessing from a service or user account that did not log on interactively. When key containers are created, most CSPs do not automatically create any <a href="/windows/desktop/SecGloss/p-gly">public/private key pairs</a>. These keys must be created as a separate step with the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DELETEKEYSET"></a><a id="crypt_deletekeyset"></a><dl>
<dt><b>CRYPT_DELETEKEYSET</b></dt>
</dl>
</td>
<td width="60%">
Delete the <a href="/windows/desktop/SecGloss/k-gly">key container</a> specified by <i>pszContainer</i>. If <i>pszContainer</i> is <b>NULL</b>, the key container with the default name is deleted. All <a href="/windows/desktop/SecGloss/k-gly">key pairs</a> in the key container are also destroyed. 




When this flag is set, the value returned in <i>phProv</i> is undefined, and thus, the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a> function need not be called afterward.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SILENT"></a><a id="crypt_silent"></a><dl>
<dt><b>CRYPT_SILENT</b></dt>
</dl>
</td>
<td width="60%">
The application requests that the CSP not display any user interface (UI) for this <a href="/windows/desktop/SecGloss/c-gly">context</a>. If the CSP must display the UI to operate, the call fails and the NTE_SILENT_CONTEXT error code is set as the last error. In addition, if calls are made to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> with the CRYPT_USER_PROTECTED flag with a context that has been acquired with the CRYPT_SILENT flag, the calls fail and the CSP sets NTE_SILENT_CONTEXT.

CRYPT_SILENT is intended for use with applications for which the UI cannot be displayed by the CSP.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DEFAULT_CONTAINER_OPTIONAL"></a><a id="crypt_default_container_optional"></a><dl>
<dt><b>CRYPT_DEFAULT_CONTAINER_OPTIONAL</b></dt>
</dl>
</td>
<td width="60%">
Obtains a context for a smart card CSP that can be used for hashing and symmetric key operations but cannot be used for any operation that requires authentication to a smart card using a PIN. This type of context is most often used to perform operations on an empty smart card, such as setting the PIN by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>. This flag can only be used with smart card CSPs. 


<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.



</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by NTE are generated by the particular CSP being used. Some possible error codes defined in Winerror.h follow.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
<dt>107L</dt>
</dl>
</td>
<td width="60%">
Some CSPs set this error if the CRYPT_DELETEKEYSET flag value is set and another thread or <a href="/windows/desktop/SecGloss/p-gly">process</a> is using this <a href="/windows/desktop/SecGloss/k-gly">key container</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
The profile of the user is not loaded and cannot be found. This happens when the application impersonates a user, for example, the IUSR_<i>ComputerName</i> account.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87L</dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
<dt>8L</dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory during the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
<dt>0x80090009L</dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter has a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY_STATE</b></dt>
<dt>0x8009000BL</dt>
</dl>
</td>
<td width="60%">
The user password has changed since the private keys were encrypted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEYSET</b></dt>
<dt>0x80090016L</dt>
</dl>
</td>
<td width="60%">
The key container could not be opened. A common cause of this error is that the key container does not exist. To create a key container, call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> using the CRYPT_NEWKEYSET flag. This error code can also indicate that access to an existing key container is denied. Access rights to the container can be granted by the key set creator by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEYSET_PARAM</b></dt>
<dt>0x8009001FL</dt>
</dl>
</td>
<td width="60%">
The <i>pszContainer</i> or <i>pszProvider</i> parameter is set to a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_PROV_TYPE</b></dt>
<dt>0x80090014L</dt>
</dl>
</td>
<td width="60%">
The value of the <i>dwProvType</i> parameter is out of range. All provider types must be from 1 through 999, inclusive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_SIGNATURE</b></dt>
<dt>0x80090006L</dt>
</dl>
</td>
<td width="60%">
The provider DLL signature could not be verified. Either the DLL or the digital signature has been tampered with.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_EXISTS</b></dt>
<dt>0x8009000FL</dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is CRYPT_NEWKEYSET, but the key container already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_KEYSET_ENTRY_BAD</b></dt>
<dt>0x8009001AL</dt>
</dl>
</td>
<td width="60%">
The <i>pszContainer</i> key container was found but is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_KEYSET_NOT_DEF</b></dt>
<dt>0x80090019L</dt>
</dl>
</td>
<td width="60%">
The requested provider does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
<dt>0x8009000EL</dt>
</dl>
</td>
<td width="60%">
The CSP ran out of memory during the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_PROV_DLL_NOT_FOUND</b></dt>
<dt>0x8009001EL</dt>
</dl>
</td>
<td width="60%">
The provider DLL file does not exist or is not on the current path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_PROV_TYPE_ENTRY_BAD</b></dt>
<dt>0x80090018L</dt>
</dl>
</td>
<td width="60%">
The provider type specified by <i>dwProvType</i> is corrupt. This error can relate to either the user default CSP list or the computer default CSP list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_PROV_TYPE_NO_MATCH</b></dt>
<dt>0x8009001BL</dt>
</dl>
</td>
<td width="60%">
The provider type specified by <i>dwProvType</i> does not match the provider type found. Note that this error can only occur when <i>pszProvider</i> specifies an actual CSP name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_PROV_TYPE_NOT_DEF</b></dt>
<dt>0x80090017L</dt>
</dl>
</td>
<td width="60%">
No entry exists for the provider type specified by <i>dwProvType</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_PROVIDER_DLL_FAIL</b></dt>
<dt>0x8009001DL</dt>
</dl>
</td>
<td width="60%">
The provider DLL file could not be loaded or failed to initialize.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_SIGNATURE_FILE_BAD</b></dt>
<dt>0x8009001CL</dt>
</dl>
</td>
<td width="60%">
An error occurred while loading the DLL file image, prior to verifying its signature.

</td>
</tr>
</table>

## -remarks

The <i>pszContainer</i> parameter specifies the name of the container that is used to hold the key. Each container can contain one key. If  you  specify the name of an existing container when creating keys, the new key will overwrite a previous one.

The combination of the CSP name and the key container name uniquely identifies a single key on the system. If one application tries to modify a key container while another application is using it, unpredictable behavior may result.

If you set the  <i>pszContainer</i> parameter to <b>NULL</b>, the default key container name is used. When the Microsoft software CSPs are called in this manner, a new container is created each time the <b>CryptAcquireContext</b> function is called. However, different CSPs may behave differently in this regard. In particular, a CSP may have a single default container that is shared by all applications accessing the CSP. Therefore, applications must not use the default key container to store private keys. Instead, either prevent key storage by passing the <b>CRYPT_VERIFYCONTEXT</b> flag in the <i>dwFlags</i> parameter, or use an application-specific container that is unlikely to be used by another application.

An application can obtain the name of the key container in use by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function to read the PP_CONTAINER value.

For performance reasons, we recommend that you set the <i>pszContainer</i> parameter to <b>NULL</b> and the <i>dwFlags</i> parameter to <b>CRYPT_VERIFYCONTEXT</b> in all situations where you do not require a persisted key. In particular, consider setting the  <i>pszContainer</i> parameter to <b>NULL</b> and the <i>dwFlags</i> parameter to <b>CRYPT_VERIFYCONTEXT</b> for the following scenarios:

<ul>
<li>You are creating a hash.
</li>
<li>You are generating a symmetric key to encrypt or decrypt data.
</li>
<li>You are deriving a symmetric key from a hash to encrypt or decrypt data.
</li>
<li>You are verifying a signature. It is possible to import a public key from a PUBLICKEYBLOB or from a certificate by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2">CryptImportPublicKeyInfo</a>.
 A context can be acquired by using the <b>CRYPT_VERIFYCONTEXT</b> flag if you only plan to import the public key.</li>
<li>You plan to export a symmetric key, but not import it within the crypto context's lifetime. A context can be acquired by using the <b>CRYPT_VERIFYCONTEXT</b> flag if you only plan to import the public key for the last two scenarios. 
</li>
<li>You are performing private key operations, but you are not using a persisted private key that is stored in a key container. </li>
</ul>
If you plan to perform private key operations, the best way to acquire a context is to try to open the container. If this attempt fails with NTE_BAD_KEYSET, then create the container by using the <b>CRYPT_NEWKEYSET</b> flag.


#### Examples

The following example shows acquiring a cryptographic context and access to public/private key pairs in a key container. If the requested key container does not exist, it is created.


For an example that includes the complete context for this example, see <a href="/windows/desktop/SecCrypto/example-c-program-creating-a-key-container-and-generating-keys">Example C Program: Creating a Key Container and Generating Keys</a>. For additional examples, see 
<a href="/windows/desktop/SecCrypto/example-c-program-using-cryptacquirecontext">Example C Program: Using CryptAcquireContext</a>.


```cpp
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hCryptProv = NULL;        // handle for a cryptographic
                                     // provider context
LPCSTR UserName = "MyKeyContainer";  // name of the key container
                                     // to be used
//-------------------------------------------------------------------
// Attempt to acquire a context and a key
// container. The context will use the default CSP
// for the RSA_FULL provider type. DwFlags is set to zero
// to attempt to open an existing key container.

if(CryptAcquireContext(
   &hCryptProv,               // handle to the CSP
   UserName,                  // container name 
   NULL,                      // use the default provider
   PROV_RSA_FULL,             // provider type
   0))                        // flag values
{
    printf("A cryptographic context with the %s key container \n", 
  UserName);
    printf("has been acquired.\n\n");
}
else
{ 
//-------------------------------------------------------------------
// An error occurred in acquiring the context. This could mean
// that the key container requested does not exist. In this case,
// the function can be called again to attempt to create a new key 
// container. Error codes are defined in Winerror.h.
 if (GetLastError() == NTE_BAD_KEYSET)
 {
   if(CryptAcquireContext(
      &hCryptProv, 
      UserName, 
      NULL, 
      PROV_RSA_FULL, 
      CRYPT_NEWKEYSET)) 
    {
      printf("A new key container has been created.\n");
    }
    else
    {
      printf("Could not create a new key container.\n");
      exit(1);
    }
  }
  else
  {
      printf("A cryptographic service handle could not be "
          "acquired.\n");
      exit(1);
   }
  
} // End of else.
//-------------------------------------------------------------------
// A cryptographic context and a key container are available. Perform
// any functions that require a cryptographic provider handle.

//-------------------------------------------------------------------
// When the handle is no longer needed, it must be released.

if (CryptReleaseContext(hCryptProv,0))
{
  printf("The handle has been released.\n");
}
else
{
  printf("The handle could not be released.\n");
}
```

> [!NOTE]
> The wincrypt.h header defines CryptAcquireContext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a>

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a>

<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>
