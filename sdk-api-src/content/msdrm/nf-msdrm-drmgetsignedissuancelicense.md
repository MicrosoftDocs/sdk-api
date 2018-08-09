---
UID: NF:msdrm.DRMGetSignedIssuanceLicense
title: DRMGetSignedIssuanceLicense function
author: windows-sdk-content
description: Acquires a signed issuance license online or offline, or produces an unsigned issuance license that can be signed later.
old-location: rm\drmgetsignedissuancelicense.htm
old-project: adrms_sdk
ms.assetid: 3ed180d1-27c9-4f39-b353-1d417636ca62
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMGetSignedIssuanceLicense, DRMGetSignedIssuanceLicense function [Active Directory Rights Management Services SDK 1.0], DRM_AUTO_GENERATE_KEY, DRM_OWNER_LICENSE_NOPERSIST, DRM_REUSE_KEY, DRM_SERVER_ISSUANCELICENSE, DRM_SIGN_CANCEL, DRM_SIGN_OFFLINE, DRM_SIGN_ONLINE, msdrm/DRMGetSignedIssuanceLicense, rm.drmgetsignedissuancelicense
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetSignedIssuanceLicense
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetSignedIssuanceLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetSignedIssuanceLicense</b> function acquires a signed issuance license online or offline, or produces an unsigned issuance license that can be signed later.


## -parameters




### -param hEnv [in]

A handle to a secure environment created by using the <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a> function. The handle is required for offline signing and optional for online signing. Applications that do not use a lockbox should pass <b>NULL</b> for this parameter.


### -param hIssuanceLicense [in]

A handle to an issuance license to sign, created by using the <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> function.


### -param uFlags [in]

Contains various options for acquiring the signed issuance license. This parameter can be one of the following values (although <b>DRM_AUTO_GENERATE_KEY</b> and <b>DRM_OWNER_LICENSE_NOPERSIST</b> can be combined with other flags). If <b>DRM_AUTO_GENERATE_KEY</b> is not specified, you must provide your own content key with a cryptographic system, such as the CryptoAPI functions.



#### DRM_SIGN_ONLINE

Specifies an online issuance license signing request from an Active Directory Rights Management Services (AD RMS) service. This flag cannot be combined with the <b>DRM_SIGN_OFFLINE</b> or <b>DRM_SERVER_ISSUANCELICENSE</b> flags.

<div class="alert"><b>Note</b>  If the AD RMS client and server versions are not identical, a license cannot be signed online. For example, a version 1.0 client cannot have a license signed online with a version 1.0 SP1 server. If the client and server versions do not match, the license must be signed offline.</div>
<div> </div>


#### DRM_SIGN_OFFLINE

Specifies an offline issuance license signing request. When signing offline, the issuance license is signed by using the <a href="c_gly.htm">client licensor certificate</a> (CLC) obtained during a previous call to <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>. To get this certificate from the store, use <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>. Each CLC is tied to the server that issued it; be sure that you are using the correct client licensor certificate for the issuance license you are publishing.

This flag cannot be combined with the <b>DRM_SIGN_ONLINE</b> or <b>DRM_SERVER_ISSUANCELICENSE</b> flags.



#### DRM_SERVER_ISSUANCELICENSE

Specifies that the unsigned issuance license be passed to the callback function. The issuance license is never signed, and the action occurs offline. This issuance license can be stored directly or used as input to <a href="https://msdn.microsoft.com/6667bab3-5022-4279-846a-61a0a37e9d33">DRMGetIssuanceLicenseTemplate</a> to create a template or used in a call to  <a href="https://msdn.microsoft.com/1dc1dc7f-4e63-4cc6-aa34-a8e44ce79655">AcquireIssuanceLicense</a>.

This flag cannot be combined with the <b>DRM_SIGN_ONLINE</b> or <b>DRM_SIGN_OFFLINE</b> flags.



#### DRM_SIGN_CANCEL

Cancels an online signing request. Offline requests are processed immediately and do not need to be canceled.



#### DRM_AUTO_GENERATE_KEY

Can be used with one of the preceding flags to have the Active Directory Rights Management Services system generate a content key for you. This key is used in encryption functions. Typically, the key type  is AES and the cipher mode is ECB. If this flag is not specified, you must provide your own content key with a cryptographic system, such as with the CryptoAPI functions from the Platform SDK.

<div class="alert"><b>Note</b>  If you are using the AD RMS client included in  Windows 7,  or if you install the <a href="http://go.microsoft.com/fwlink/p/?linkid=155817">CBC hotfix</a>, the value AES_CBC4K can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a> code examples for more information.</div>
<div> </div>


#### DRM_OWNER_LICENSE_NOPERSIST

The owner license is stored in memory instead of the permanent store. The owner license can subsequently be retrieved by the <a href="https://msdn.microsoft.com/e657ac08-9635-40ac-8d9f-cc8ab9ed3a6c">DRMGetOwnerLicense</a> function.



#### DRM_REUSE_KEY

Causes the content key to be reused. The content key is obtained from the signed issuance license associated with the bound license (<i>hBoundLicense</i>) that is passed in to <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>. You must ensure that the bound license is bound to either the <b>EDITRIGHTSDATA</b> or <b>OWNER</b> right. This flag is available only in Windows 7.

<div class="alert"><b>Note</b>  This flag must be combined with <b>DRM_SIGN_OFFLINE</b>. You can also optionally combine it with <b>DRM_OWNER_LICENSE_NOPERSIST</b>. These are the only allowed values. The parameters <i>pbSymKey</i> and <i>cbSymKey</i> must be set to 0. See the code sample  in this topic.</div>
<div> </div>
<div class="alert"><b>Caution</b>  To avoid security implications, reuse the content key only if users or rights are being added. Additionally, it is a best practice to always generate a new content identifier for the publishing license to avoid an older end-user license being used with the new publishing license.</div>
<div> </div>

### -param pbSymKey [in]

The content key used to encrypt the document. If this value is <b>NULL</b>, the <i>uFlags</i> parameter must specify <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>. These <i>uFlags</i> values cause <i>pbSymKey</i> to be ignored.


### -param cbSymKey [in]

The size, in bytes, of the content key. Currently, this parameter can only be 16 unless the <i>uFlags</i> parameter specifies <b>DRM_AUTO_GENERATE_KEY</b> or <b>DRM_REUSE_KEY</b>, in which case this parameter can be zero.


### -param wszSymKeyType [in]

The key type. The value <b>AES</b> specifies the Advanced Encryption Standard (AES) algorithm with the  electronic code book (ECB) cipher mode. If you are using Windows 7, the value <b>AES_CBC4K</b> can be used to specify the AES algorithm with cipher-block chaining (CBC) cipher mode. See the <a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a> code examples for more information.


### -param wszClientLicensorCertificate [in]

A pointer to null-terminated Unicode string that contains a client licensor certificate obtained by using the <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a> function. If you are attempting online signing, this parameter should be <b>NULL</b>. If you are developing a server application that does not use a lockbox and  if you are using the <b>DRM_SERVER_ISSUANCELICENSE</b> flag in <i>uFlags</i>, pass in the server license certificate chain. The server licensor certificate chain can be retrieved by using the <a href="https://msdn.microsoft.com/bf0984e0-419c-49a0-b681-46630af25f67">GetLicensorCertificate</a> SOAP method; however, to make the chain usable, it must be reordered by using the <a href="https://msdn.microsoft.com/27c2bf2e-54b1-4ed4-a754-e8b3b3bd58cb">DRMConstructCertificateChain</a> function.


### -param pfnCallback [in]

A pointer to the callback function used to notify the application of an asynchronous request's progress. For the signature of the callback function you must provide, see <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>.


### -param wszURL [in]

A pointer to a null-terminated Unicode string that contains the URL of an AD RMS licensing server that was obtained by using the <a href="https://msdn.microsoft.com/f7cbc3ba-009f-4a35-999e-139d41961fd9">DRMGetServiceLocation</a> function. This string takes the form "<i>ADRMSLicensingServerURL</i>/_wmcs/Licensing". This parameter value is required for online license requests; you can use <b>NULL</b> for offline license requests. This URL is entered in the signed issuance license as the default silent license acquisition URL, which is where an application will automatically go to acquire an end-user license if none is specified in <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>.


### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The application callback function specified in the <i>pfnCallback</i> parameter will be called with the <a href="https://msdn.microsoft.com/0d61bd67-74d7-4c13-834d-94154ac9b527">DRM_MSG_SIGN_ISSUANCE_LICENSE</a> message to provide status feedback. This is an asynchronous function that will return either a signed or an unsigned issuance license to the callback function after <b>DRMGetSignedIssuanceLicense</b> has returned.

You request an unsigned issuance license when you want to obtain the string value of an unsigned issuance license from its handle, for example, if you want to call the <a href="https://msdn.microsoft.com/1dc1dc7f-4e63-4cc6-aa34-a8e44ce79655">AcquireIssuanceLicense</a> SOAP method, or the <a href="https://msdn.microsoft.com/6667bab3-5022-4279-846a-61a0a37e9d33">DRMGetIssuanceLicenseTemplate</a> function.

The retrieved license is not persisted in the permanent license store; the application must obtain the license in the callback function and handle storage. An application uses this function for publishing. If the issuance license owner (the user referenced in <i>hOwner</i> in the <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> function) calls this function for a signed issuance license, they will receive a use license (deposited in the license store) as well as a signed issuance license in the callback function.

When a user calls this function, the issuance license is signed by an AD RMS service (online) or by a client licensor certificate issued by an AD RMS service (offline), and the content key is encrypted by the server's public key. The server licensor certificate of the server that will be signing the unsigned issuance license can take the place of the client licensor certificate when this function is called by a server application that is not using a lockbox. A server application that does not use a lockbox cannot use this function to obtain a signed issuance license offline.

The application can either supply its own content key, or request that AD RMS create one for it. If you are creating your own key, be sure to create a new content key for each piece of content you want to encrypt. AES is currently the only key type supported by AD RMS.

If this call goes out of the caller's intranet to an Internet location that is not on the user's trusted sites list, a security password dialog box will be presented to the user. A URL is considered to be out of the user's domain if the domain of the URL is fully qualified (for example, the fully qualified https://licensing.contoso.com/_wmcs/licensing, instead of the internal URL https://licensing/_wmcs/licensing). Locations inside the user's domain are implicitly trusted; locations outside the user's domain must be explicitly trusted. If an intranet administrator wants to use a service outside the expected user's trust zone, the administrator should consider using a domain group policy to add the company server to the trusted sites for those users.

An issuance license must contain metadata before it can be signed. Typical metadata contains the ID, type, and name of an item of content. If you create the license from scratch, you must manually add metadata by calling the <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a> function. If you create the license from a template or from an existing license, the metadata contained there is automatically added to the new issuance license, but you should call <b>DRMSetMetaData</b> to assign a new content ID. For more information, see <a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>.

The following code sample shows how to use the <b>DRM_REUSE_KEY</b> value for <i>uFlags</i> to specify that the content key should be reused. This functionality is available only with Windows 7.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
extern HRESULT __stdcall StatusCallback( 
               DRM_STATUS_MSG msg, 
               HRESULT hr, 
               void *pvParam, 
               void *pvContext 
               );

/*===================================================================
Function:      EditSignedIL

THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.
===================================================================*/

/////////////////////////////////////////////////////////////////////
// The EditSignedIL function edits a signed issuance license by adding
// a user while retaining the content key so that content protected
// using the issuance license does not have to be re-encrypted.
//
// Arguments:
//        hEnv                  - [in]  Environment handle
//        pwszUserID            - [in]  User email address that needs 
//                                      to be added to the IL
//        pwszUserRight         - [in]  Right that needs to be granted
//        pwszRAC               - [in]  RAC of the Republishing user
//        pwszCLC               - [in]  CLC of the Republishing user
//        pwszOldSignedIL       - [in]  Old Signed Issuance License
//        pwszEUL               - [in]  Use License of the Republishing 
//                                      user with EDITRIGHTSDATA or OWNER
//        ppwszNewSignedIL      - [out] New Signed Issuance License 

HRESULT EditSignedIL(DRMENVHANDLE hEnv,                        
                       PWSTR        pwszUserID,
                       PWSTR        pwszUserRight,
                       PWSTR        pwszRAC,
                       PWSTR        pwszCLC,
                       PWSTR        pwszOldSignedIL,
                       PWSTR        pwszEUL,
                       PWSTR        *ppwszNewSignedIL)
{
    HRESULT       hr                    = S_OK; // HRESULT return code
    DRMPUBHANDLE  hOldIssuanceLicense   = NULL; // Issuance license handle
    DRMPUBHANDLE  hNewIssuanceLicense   = NULL; // Issuance license handle
    DRMPUBHANDLE  hUser                 = NULL; // User handle
    DRMPUBHANDLE  hRight                = NULL; // Right handle
    const UINT    GUID_LENGTH           = 128;  // GUID string length
    PWSTR         pwszNewContentId      = NULL; // Unique content ID for new IL
    UINT          uiNewContentId        = 0;    // content id length
    GUID          guid;                         // Raw Guid: unique content ID
    const DWORD   DW_WAIT_TIME          = 60000;// Maximum signal duration
    DWORD         dwWaitResult          = 0;    // Actual signal duration
    SYSTEMTIME    stTimeFrom;                   // Validity period start
    SYSTEMTIME    stTimeUntil;                  // Validity period end
    DRM_CONTEXT   context;                      // Callback context
    DRMHANDLE     hBoundLicense         = NULL; // Bound License handle
    DRMHANDLE     hDecryptor            = NULL; // Decryptor handle    
    UINT          uiOldContentId        = 0;    // Content Id Length of Old IL
    UINT          uiOldContentIdType    = 0;    // Content Id Type Length of Old IL
    PWSTR         pwszOldContentId      = NULL; // Content Id of old IL
    PWSTR         pwszOldContentIdType  = NULL; // Content Id Type of old IL
    DRMID         idOldContent;                 // Content Id structure
    PWSTR         pwszSymmKeyType       = NULL; // Symmetric Key Type 
    UINT          cbSymmKeyType         = 0;    // Symmetric Key Type Length
    DRMENCODINGTYPE encodingType;               // Encoding Type
    DRMBOUNDLICENSEPARAMS     bParams;          // Bound License parameters

    wprintf(L"\r\nEntering EditSignedIL. \r\n");

    // Initialize the callback context.
    SecureZeroMemory(&amp;context, sizeof(context));

    // Get the system time for the starting and ending times that
    // specify the validity period of the unsigned issuance license.
    // Add one year to the ending time.
    GetSystemTime( &amp;stTimeFrom );
    GetSystemTime( &amp;stTimeUntil );
    stTimeUntil.wYear++;

    // Obtain the Content Id from the Signed issuance license
    //          a. Create an issuance license handle from the signed IL
    //          b. Obtain content ID and content ID Type
    hr = DRMCreateIssuanceLicense( 
          &amp;stTimeFrom,                // Starting validity time
          &amp;stTimeUntil,               // Ending validity time
          NULL,                       // Not supported
          NULL,                       // Not supported
          NULL,                       // Handle to license owner
          pwszOldSignedIL,            // Existing issuance license
          NULL,                       // Bound license handle
          &amp;hOldIssuanceLicense);      // Handle to the license
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateIssuanceLicense: hOldIssuanceLicense = %i \r\n",
          hOldIssuanceLicense);

    hr = DRMGetMetaData(
          hOldIssuanceLicense,        // Handle to the license
          &amp;uiOldContentId,            // Content Id Length
          NULL,                       // Content Id
          &amp;uiOldContentIdType,        // Content Id Type Length
          NULL,                       // Content Id Type 
          NULL,                       // SKU ID Length
          NULL,                       // SKU ID 
          NULL,                       // SKU ID Type Length
          NULL,                       // SKU ID Type
          NULL,                       // Content Type Length
          NULL,                       // Content Type
          NULL,                       // Content Name Length
          NULL);                      // Content Name 
    if(FAILED(hr)) goto e_Exit;

    pwszOldContentId = new WCHAR[uiOldContentId];
    if(NULL == pwszOldContentId) 
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    pwszOldContentIdType = new WCHAR[uiOldContentIdType];
    if(NULL == pwszOldContentIdType) 
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    hr = DRMGetMetaData(
          hOldIssuanceLicense,        // Handle to the license
          &amp;uiOldContentId,            // Content Id Length
          pwszOldContentId,           // Content Id
          &amp;uiOldContentIdType,        // Content Id Type Length
          pwszOldContentIdType,       // Content Id Type 
          NULL,                       // SKU ID Length
          NULL,                       // SKU ID 
          NULL,                       // SKU ID Type Length
          NULL,                       // SKU ID Type
          NULL,                       // Content Type Length
          NULL,                       // Content Type
          NULL,                       // Content Name Length
          NULL);                      // Content Name 
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMGetMetadata: pwszOldContentId = %ws \r\n",
          pwszOldContentId);

    // Create the content id structure for the BOUNDLICENSEPARAMS
    idOldContent.uVersion  = 0; 
    idOldContent.wszIDType = pwszOldContentIdType; 
    idOldContent.wszID     = pwszOldContentId; 

    // Bind the license to the EDITRIGHTSDATA or OWNER right 
    // to reuse the key. 
    bParams.hEnablingPrincipal                     = NULL; 
    bParams.hSecureStore                           = NULL; 
    bParams.wszRightsRequested                     = L"EDITRIGHTSDATA";  
    bParams.wszRightsGroup                         = L"Main-Rights"; 
    bParams.idResource                             = idOldContent; 
    bParams.wszDefaultEnablingPrincipalCredentials = pwszRAC; 
    bParams.cAuthenticatorCount                    = 0; 

    hr = DRMCreateBoundLicense( 
        hEnv,                    // secure environment handle 
        &amp;bParams,                // additional license options 
        pwszEUL,                 // owner license 
        &amp;hBoundLicense,          // handle to bound license 
        NULL                     // reserved 
        ); 
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateBoundLicense: hBoundLicense = %i \r\n",
          hBoundLicense);

    hr = DRMCreateEnablingBitsDecryptor( 
        hBoundLicense,           // bound license handle 
        NULL,                    // right name
        NULL,                    // reserved
        NULL,                    // reserved
        &amp;hDecryptor              // decryptor handle 
        ); 
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateEnablingBitsDecryptor: hDecryptor = %i \r\n",
          hDecryptor);

    // Obtain the key type set in the decryptor so that it can be 
    // specified when creating the new issuance license
    // g_wszQUERY_SYMMETRICKEYTYPE requires a client that supports 
    // AES-CBC4K. Otherwise, symmetric key type can always be assumed 
    // to be "AES"
    hr = DRMGetInfo(hDecryptor,
                    g_wszQUERY_SYMMETRICKEYTYPE,
                    &amp;encodingType,
                    &amp;cbSymmKeyType,
                    NULL);
    if(FAILED(hr)) goto e_Exit;

    pwszSymmKeyType = new WCHAR[cbSymmKeyType / 2];
    if(pwszSymmKeyType == NULL) 
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }
    SecureZeroMemory(pwszSymmKeyType, cbSymmKeyType);

    hr = DRMGetInfo(hDecryptor,
                    g_wszQUERY_SYMMETRICKEYTYPE,
                    &amp;encodingType,
                    &amp;cbSymmKeyType,
                    (BYTE*)pwszSymmKeyType);
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMGetInfo: pwszSymmKeyType = %ws \r\n",
          pwszSymmKeyType);

    // Create an unsigned issuance license from the passed in
    // signed issuance license.
    hr = DRMCreateIssuanceLicense( 
          &amp;stTimeFrom,           // Starting validity time
          &amp;stTimeUntil,          // Ending validity time
          NULL,                  // Not supported
          NULL,                  // Not supported
          NULL,                  // Handle to license owner
          pwszOldSignedIL,       // Existing issuance license
          hBoundLicense,         // Bound license: get rights 
                                 // and content key 
          &amp;hNewIssuanceLicense); // Handle to the new license
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateIssuanceLicense: hNewIssuanceLicense = %i \r\n",
          hNewIssuanceLicense);

    // Create a GUID to use as the unique content ID.
    hr = CoCreateGuid(&amp;guid);
    if(FAILED(hr)) goto e_Exit;

    pwszNewContentId = new WCHAR[GUID_LENGTH];
    if (NULL == pwszNewContentId)
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    uiNewContentId = StringFromGUID2( guid, pwszNewContentId, GUID_LENGTH );
    if (0 == uiNewContentId)
    {
        hr = E_FAIL;
        goto e_Exit;
    }
    wprintf(L"StringFromGUID2: pwszNewContentId = %s \r\n", pwszNewContentId);

    // Set your metadata in the unsigned issuance license.
    hr = DRMSetMetaData(
          hNewIssuanceLicense,        // Issuance license handle
          pwszNewContentId,           // Unique content ID
          L"MS-GUID",                 // Type of content ID
          L"SKUId",                   // SKU ID
          L"SKUIdType",               // SKU ID type
          L"ContentType",             // Content type
          L"ContentName");            // Content name
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMSetMetaData succeeded. \r\n");

    // Create a user handle.
    hr = DRMCreateUser(
          pwszUserID,                 // User ID or name
          NULL,                       // Verified ID
          L"Windows",                 // Type of user ID
          &amp;hUser );                   // Handle to the user
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateUser:  hUser = %i \r\n", hUser);

    // Create a right.
    hr = DRMCreateRight( 
          pwszUserRight,              // Name of the right to create
          &amp;stTimeFrom,                // Starting validity time
          &amp;stTimeUntil,               // Ending validity time
          0,                          // No extended information
          NULL,                       // Extended information name
          NULL,                       // Extended information value
          &amp;hRight );                  // Handle to the created right
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMCreateRight:  hRight = %i \r\n", hRight);

    // Associate the right with the user and add both to the 
    // unsigned issuance license.
    hr = DRMAddRightWithUser( 
          hNewIssuanceLicense,        // Issuance license handle
          hRight,                     // Right from DRMCreateRight
          hUser );                    // User from DRMCreateUser
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMAddRightWithUser succeeded. \r\n");

    // Create an event to signal when the license has been signed.
    context.hEvent = CreateEvent(
          NULL,                       // No attributes
          FALSE,                      // Automatic reset
          FALSE,                      // Initial state not signaled
          NULL);                      // Event object not named
    if(NULL == context.hEvent) goto e_Exit;

    // Sign the issuance license offline by using the client
    // licensor certificate
    hr = DRMGetSignedIssuanceLicense( 
          hEnv,                  // Environment handle
          hNewIssuanceLicense,   // Issuance license handle
          DRM_SIGN_OFFLINE |     // Sign offline with a CLC
                DRM_REUSE_KEY,   // Reuse content key from old IL
          NULL,                  // No symmetric key specified
          0,                     // No length specified
          pwszSymmKeyType,       // Pass in same key type as old IL
          pwszCLC,               // Client licensor certificate
          &amp;StatusCallback,       // Callback function
          NULL,                  // No licensing URL specified
          (void*)&amp;context);      // Callback context parameter
    if(FAILED(hr)) goto e_Exit;
    wprintf(L"DRMGetSignedIssuanceLicense succeeded. \r\n");

    // Wait for the callback to return.
    dwWaitResult = WaitForSingleObject(context.hEvent, DW_WAIT_TIME);
    if(WAIT_TIMEOUT == dwWaitResult) 
    {
        hr = E_FAIL;
        goto e_Exit;
    }

    if(FAILED(context.hr))
    {
        hr = context.hr;
        goto e_Exit;
    }

    // Assign the license pointer to the output parameter. 
    *ppwszNewSignedIL = context.wszData;
    context.wszData = NULL;

e_Exit:
    if(NULL != context.hEvent)
    {
        CloseHandle(context.hEvent);
    }
    if(NULL != context.wszData)
    {
        delete[] context.wszData;
    }
    if(NULL != pwszOldContentId)
    {
        delete[] pwszOldContentId;
    }
    if(NULL != pwszOldContentIdType)
    {
        delete[] pwszOldContentIdType;
    }
    if(NULL != pwszSymmKeyType)
    {
        delete[] pwszSymmKeyType;
    }
    if(NULL != hDecryptor)
    {
        DRMCloseHandle(hDecryptor);
    }
    if(NULL != hBoundLicense)
    {
        DRMCloseHandle(hBoundLicense);
    }
    if(NULL != hOldIssuanceLicense)
    {
        DRMClosePubHandle(hOldIssuanceLicense);
    }
    if(NULL != hNewIssuanceLicense)
    {
        DRMClosePubHandle(hNewIssuanceLicense);
    }
    if(NULL != hUser)
    {
        DRMClosePubHandle(hUser);
    }
    if(NULL != hRight)
    {
        DRMClosePubHandle(hRight);
    }
    if(NULL != pwszNewContentId)
    {
        delete [] pwszNewContentId;
    }
    wprintf(L"Leaving EditSignedIL: hr = %x \r\n", hr);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/a156994b-e6a8-42dc-8a49-cae20ea2e9da">Offline Signing Code Example</a>



<a href="https://msdn.microsoft.com/93b509a5-4997-46cd-823f-5529ec966ac6">Online Signing Code Example</a>
 

 

