---
UID: NF:msdrm.DRMEncrypt
title: DRMEncrypt function (msdrm.h)
description: Encrypts data.
helpviewer_keywords: ["DRMEncrypt","DRMEncrypt function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMEncrypt","rm.drmencrypt"]
old-location: rm\drmencrypt.htm
tech.root: rm
ms.assetid: 1de19409-2b14-4ab0-9853-23ee5741a7ae
ms.date: 12/05/2018
ms.keywords: DRMEncrypt, DRMEncrypt function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMEncrypt, rm.drmencrypt
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMEncrypt
 - msdrm/DRMEncrypt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMEncrypt
---

# DRMEncrypt function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMEncrypt</b> function encrypts data.

## -parameters

### -param hCryptoProvider [in]

A handle to an AD RMS encrypting object created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsencryptor">DRMCreateEnablingBitsEncryptor</a> function.

### -param iPosition [in]

Position in the buffer at which to start encrypting. <b>0</b> corresponds to the first block in a buffer, <b>1</b> corresponds to the second block, and so on. 

<div class="alert"><b>Note</b>  If you use the <b>AES</b> key when you sign the issuance license, <i>iPosition</i> can always be set to 0.</div>
<div> </div>

### -param cNumInBytes [in]

The number of bytes to encrypt.

### -param pbInData [in]

A pointer to a buffer that contains the bytes to encrypt.

### -param pcNumOutBytes [in, out]

The number of encrypted bytes.

### -param pbOutData [out]

A pointer to the encrypted bytes.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Memory allocation and release of the encrypted content is the responsibility of the calling function. The following code sample, from <a href="/previous-versions/windows/desktop/adrms_sdk/encrypting-content">Encrypting Content</a>, shows how to encrypt content in blocks. This particular example already knows the size of the content to encrypt and allocates memory beforehand. If you must determine the number of bytes to allocate, however,  the required buffer size is returned in the <i>pcNumOutBytes</i> parameter after the first call. Allocate memory and call the function again with  <i>pbOutData</i> set to point to the new memory.


```cpp

#include "EncryptingContent.h"

/*===================================================================
File:      Encryption_EncryptContent.cpp

THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.
===================================================================*/

/////////////////////////////////////////////////////////////////////
// The EncryptContent function encrypts content. In this example,
// the content to be encrypted is defined in the header file.
//   #define PLAINTEXT L"This is the content to be encrypted."
//
HRESULT EncryptContent(
          DRMENVHANDLE   hEnv,
          DRMHANDLE      hLib,
          PWSTR          pwszRAC,
          PWSTR          pwszGUID,
          DRMHANDLE      hIssuanceLic,
          PWSTR          pwszSignedIL,
          BYTE**         ppbEncrypted)

{
  ///////////////////////////////////////////////////////////////////
  // Declare variables:
  //   hr........................Return value                     
  //   pwszOwnerLicense..........License with OWNER right
  //   pwszOutFile...............Name of file for encrypted content
  //   pbEncrypted...............Buffer to hold encrypted content
  //   uiOwnerLicenseLength......Owner licensee length, in characters
  //   uiBlock...................Decryption block size (16 bytes)
  //   uiBytes...................Size, in bytes, of uiBlock
  //   uiPlainText...............Number of bytes in the plain text
  //   uiPadding.................Blank space added to plain text
  //   uiBuffer..................uiPlainText + uiPadding
  //   uiEncrypted...............Size, bytes, of encrypted content
  //   uiOffset..................Offset into encryption buffer
  //   pbPlainText...............Pointer to unencrypted content
  //   hBoundLicense.............Handle to license bound to OWNER
  //   hEP.......................Enabling principal for binding   
  //   hEBEncryptor..............Handle to encrypting object
  //   dwBytesWritten............WriteFile function bytes written 
  //   idNULL....................DRMID structure
  //   idContent.................Structure for binding a license
  //   idStandardEP..............Structure for enabling principal
  //   oParams...................Structure for binding a license
  //   eType.....................Structure for license encoding
  //   
  HRESULT       hr                     = E_FAIL;
  PWSTR         pwszOwnerLicense       = NULL;
  PWSTR         pwszOutFile            = L"EncryptedContent.bin";
  BYTE*         pbEncrypted            = NULL;
  UINT          uiOwnerLicenseLength   = 0;
  UINT          uiBlock                = 0;
  UINT          uiBytes                = 0;
  UINT          uiPlainText            = 0;
  UINT          uiBuffer               = 0;
  UINT          uiPadding              = 0;
  UINT          uiEncrypted            = 0;
  UINT          uiOffset               = 0;
  BYTE*         pbPlainText            = NULL;
  DRMHANDLE     hBoundLicense          = NULL; 
  DRMHANDLE     hEP                    = NULL; 
  DRMHANDLE     hEBEncryptor           = NULL;
  DWORD         dwBytesWritten         = 0;
  DRMID         idNULL;
  DRMID         idContent;
  DRMID         idStandardEP;
  DRMBOUNDLICENSEPARAMS oParams;
  DRMENCODINGTYPE eType;              

  wprintf(L"\r\nEntering EncryptContent.\r\n");
 
  // Validate the input parameters.
  if ( NULL==hEnv ||
       NULL==hLib ||
       NULL==pwszRAC ||
       NULL==pwszGUID ||
       NULL==hIssuanceLic ||
       NULL==pwszSignedIL ||
       NULL==ppbEncrypted)
       return E_INVALIDARG;

  // Create an enabling principal.
  SecureZeroMemory(&idNULL, sizeof(idNULL));
  SecureZeroMemory(&idStandardEP, sizeof(idStandardEP));
  idStandardEP.wszIDType = L"ASCII Tag"; 
  idStandardEP.wszID     = L"UDStdPlg Enabling Principal"; 

  hr = DRMCreateEnablingPrincipal ( 
          hEnv,                     // Secure environment handle 
          hLib,                     // Library handle 
          idStandardEP.wszID,       // Enabling principal type 
          &idNULL,                  // DRMID structure 
          pwszRAC,                  // Rights account certificate
          &hEP);                    // enabling principal handle 
  if(FAILED(hr)) return hr;
  wprintf(L"DRMCreateEnablingPrincipal: hEP %i \r\n", hEP);

  // Call DRMGetOwnerLicense to get a license to bind to. An owner
  // license contains the OWNER right which allows the user to
  // exercise all rights regardless of whether they have been
  // explicitly granted.
  //   - Call DRMGetOwnerLicense once to retrieve the length, in
  //     characters, of the owner license.
  //   - Allocate memory for the license.
  //   - Call DRMGetOwnerLicense again to retrieve the license.
  //   - You must release the memory before leaving this function.
  hr = DRMGetOwnerLicense( 
           hIssuanceLic,               // Issuance license handle
           &uiOwnerLicenseLength,      // License length
           NULL);                      // Not used
  if(FAILED(hr)) goto e_Exit;

  pwszOwnerLicense = new WCHAR[uiOwnerLicenseLength];
  if(NULL == pwszOwnerLicense)
  {
    hr = E_OUTOFMEMORY; 
    goto e_Exit; 
  }
  hr = DRMGetOwnerLicense( 
          hIssuanceLic, 
          &uiOwnerLicenseLength, 
          pwszOwnerLicense);
  if(FAILED(hr)) goto e_Exit;
  wprintf(L"DRMGetOwnerLicense (pwszOwnerLicense) succeeded.\r\n");

  // Bind the owner license to the OWNER right.
  SecureZeroMemory(&idContent, sizeof(idContent));
  idContent.wszIDType        = L"MS-GUID"; 
  idContent.wszID            = pwszGUID;

  SecureZeroMemory(&oParams, sizeof(oParams));
  oParams.hEnablingPrincipal = hEP; 
  oParams.wszRightsRequested = L"OWNER";
  oParams.wszRightsGroup     = L"Main-Rights"; 
  oParams.idResource         = idContent; 

  hr = DRMCreateBoundLicense ( 
          hEnv,                     // Secure environment handle 
          &oParams,                 // Additional license options 
          pwszOwnerLicense,         // Owner license 
          &hBoundLicense,           // Handle to the bound license 
          NULL );                   // Reserved
  if(FAILED(hr)) goto e_Exit;
  wprintf(L"DRMCreateBoundLicense: (hBoundLicense) succeeded.\r\n");

  // Create an encrypting object. 
  hr = DRMCreateEnablingBitsEncryptor( 
          hBoundLicense,              // Bound license handle
          oParams.wszRightsRequested, // Requested right
          NULL,                       // Reserved
          NULL,                       // Reserved
          &hEBEncryptor);             // Encrypting object handle
  if(FAILED(hr)) goto e_Exit;
  wprintf(L"DRMCreateEnablingBitsEncryptor succeeded.\r\n");

  // Retrieve the size, in bytes, of the memory block that must 
  // be passed to DRMEncrypt.
  uiBytes= sizeof(uiBlock);
  hr = DRMGetInfo(
          hEBEncryptor,               // Encrypting object handle
          g_wszQUERY_BLOCKSIZE,       // Attribute to query for
          &eType,                     // Type of encoding to apply
          &uiBytes,                   // Size of uiBlock variable
          (BYTE*)&uiBlock);           // Size of memory block
  if(FAILED(hr)) goto e_Exit;
  wprintf(L"DRMGetInfo: uiBlock = %u\r\n", uiBlock);

  // Determine the size of the buffer needed to store the
  // encrypted content. The buffer must be an even multiple of 
  // the buffer size used during the [typically] iterative 
  // encryption process. In this example, the plain text
  // is 72 bytes long and the encryption buffer is 16 bytes. 
  // However 72 % 16 = 8. The plain text must therefore be padded
  // to 80 bytes (80 % 16 = 0).
  uiPlainText = (UINT)(sizeof(WCHAR) * wcslen(PLAINTEXT));
  uiPadding = uiBlock - (uiPlainText % uiBlock);
  uiBuffer = uiPlainText + uiPadding;

  pbPlainText = new BYTE[uiBuffer];
  *ppbEncrypted = new BYTE[uiBuffer];

  SecureZeroMemory(pbPlainText, sizeof(pbPlainText));
  memcpy_s(
          pbPlainText,
          uiBuffer,
          (BYTE*)PLAINTEXT,
          uiPlainText);

  // Encrypt the plain text.
  for ( int j = 0; (UINT)j * uiBlock < uiBuffer; j++ )
  {
    hr = DRMEncrypt( 
          hEBEncryptor,               // Encrypting object handle
          j * uiBlock,                // Position in buffer
          uiBlock,                    // Number of bytes to encrypt
          pbPlainText + (j*uiBlock),  // Bytes to encrypt
          &uiEncrypted,               // Number of bytes encrypted
          NULL);                      // NULL on first call
    if(FAILED(hr)) goto e_Exit;

    hr = DRMEncrypt( 
          hEBEncryptor,               // Encrypting object handle 
          j * uiBlock,                // Position in buffer 
          uiBlock,                    // Number of bytes to encrypt
          pbPlainText + (j*uiBlock),  // Bytes to encrypt
          &uiEncrypted,               // Number of bytes encrypted
          *ppbEncrypted + uiOffset);  // Encrypted content
    if(FAILED(hr)) goto e_Exit;

    uiOffset += uiEncrypted;          // Increment the buffer offset
  }

  // Create a new file to write the encrypted content and issuance
  // license to.
  HANDLE hFile = CreateFile(
          pwszOutFile,                // File name
          GENERIC_WRITE,              // Access type
          0,                          // Require exclusive access
          NULL,                       // Default security attributes
          CREATE_ALWAYS,              // Allow write-only access
          0,                          // No file attributes or flags
          NULL);                      // No open file as template
  if(INVALID_HANDLE_VALUE == hFile)
  {
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto e_Exit;
  }
  wprintf(L"CreateFile: hFile = %i\r\n", hFile);

  // Write the encrypted content and relevant data to the file.
  if(!WriteFile(hFile, 
                &uiBuffer, 
                sizeof(UINT), 
                &dwBytesWritten, 
                NULL))
    goto e_Exit;
  size_t uiIssuanceLicenseLgth = (UINT)(sizeof(WCHAR) * 
                                 wcslen(pwszSignedIL));
  if(!WriteFile(hFile, 
                &uiIssuanceLicenseLgth, 
                sizeof(size_t), 
                &dwBytesWritten, 
                NULL))
    goto e_Exit;
  if(!WriteFile(hFile, 
                *ppbEncrypted, 
                uiBuffer, 
                &dwBytesWritten, 
                NULL))
    goto e_Exit;
  if(!WriteFile(hFile, 
                pwszSignedIL, 
                uiIssuanceLicenseLgth, 
                &dwBytesWritten, 
                NULL))
    goto e_Exit;
  wprintf(L"Writing to file succeeded.\r\n");

e_Exit:

  if (INVALID_HANDLE_VALUE != hFile)
  {
    CloseHandle(hFile);
  }
  if (NULL != hEP)
  {
    hr = DRMCloseHandle(hEP);
    hEP = NULL;
  }
  if (NULL != hBoundLicense)
  {
    hr = DRMCloseHandle(hBoundLicense);
    hBoundLicense = NULL;
  }
  if (NULL != hEBEncryptor)
  {
    hr = DRMCloseHandle(hEBEncryptor);
    hEBEncryptor = NULL;
  }
  if (NULL != pwszOwnerLicense)
  {
    delete [] pwszOwnerLicense;
    pwszOwnerLicense = NULL;
  }

  wprintf(L"Leaving EncryptContent: hr = %x \r\n", hr);
  return hr;
}

```


The following code sample shows how to use the AES algorithm with the cipher-block chaining (CBC) cipher mode to encrypt content. This functionality is available only in Windows 7.


```cpp

/*===================================================================
Functions:      PerformCbcEncryption and PerformCbcDecryption

THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.
===================================================================*/
#include "msdrm.h"
#include "msdrmgetinfo.h"

#define SZ_CBC_KEY_TYPE L"AES_CBC4K"
#define DW_WAIT_TIME 60000
#define SZ_ENABLING_PRINCIPAL_TYPE L"UDStdPlg Enabling Principal"
#define SZ_MAIN_RIGHTS_GROUP L"Main-Rights"
#define SZ_EDIT_RIGHT L"EDIT"
#define SZ_VIEW_RIGHT L"VIEW"

extern HRESULT __stdcall StatusCallback(DRM_STATUS_MSG msg,
                                        HRESULT hr,
                                        void* pvParam,
                                        void* pvContext);

//
// Struct to hold DRMGetSignedIssuanceLicense callback information
//
typedef struct Drm_Context
{
 HANDLE  hEvent;
 HRESULT hr;
 PWSTR   wszData;
} DRM_CONTEXT, *PDRM_CONTEXT;

//
// This helper function will perform steps required to get a bound
// license when provided the required information. It is listed
// here to demonstrate that this part of the CBC encryption and
// decryption flow is unchanged from the standard flow. In practice,
// since creating a new bound license for each encryption and
// decryption request is costly, you would instead obtain all
// requested rights at once in a comma-separated list and reuse
// a single bound license when possible.
//
inline HRESULT GetBoundLicense(__in DRMENVHANDLE hEnv,
                               __in PWCHAR pwszRac,
                               __in PWSTR pwszUseLicense,
                               __in PWSTR pwszRightsRequested,
                               __in DRMHANDLE hIssuanceLicense,
                               __out DRMHANDLE* phBoundLicense)
{
    HRESULT hr = S_OK;
    DRMHANDLE hEnablingPrincipal = NULL;
    DRMID idNULL(NULL, NULL);
    UINT uiContentId = 0;
    UINT uiContentIdType = 0;
    PWSTR pwszContentId = NULL;
    PWSTR pwszContentIdType = NULL;
    DRMID idContent;
    DRMBOUNDLICENSEPARAMS bParams;

    hr = DRMCreateEnablingPrincipal(
        hEnv,                       // Environment handle
        NULL,                       // No library specified
        SZ_ENABLING_PRINCIPAL_TYPE, // Enabling principal type
        &idNULL,                    // DRMID structure
        pwszRac,                    // Current user certificate / RAC
        &hEnablingPrincipal);       // Enabling principal handle
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Obtain the sizes of the buffers needed for the
    // content ID and content ID type
    hr = DRMGetMetaData(
          hIssuanceLicense,        // Handle to the license
          &uiContentId,            // Content Id Length
          NULL,                    // Content Id
          &uiContentIdType,        // Content Id Type Length
          NULL,                    // Content Id Type
          NULL,                    // SKU ID Length
          NULL,                    // SKU ID
          NULL,                    // SKU ID Type Length
          NULL,                    // SKU ID Type
          NULL,                    // Content Type Length
          NULL,                    // Content Type
          NULL,                    // Content Name Length
          NULL);                   // Content Name
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    pwszContentId = new WCHAR[uiContentId];
    if(NULL == pwszContentId) 
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    pwszContentIdType = new WCHAR[uiContentIdType];
    if(NULL == pwszContentIdType) 
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    // Obtain the content ID and content ID type
    hr = DRMGetMetaData(
          hIssuanceLicense,        // Handle to the license
          &uiContentId,            // Content Id Length
          pwszContentId,           // Content Id
          &uiContentIdType,        // Content Id Type Length
          pwszContentIdType,       // Content Id Type
          NULL,                    // SKU ID Length
          NULL,                    // SKU ID
          NULL,                    // SKU ID Type Length
          NULL,                    // SKU ID Type
          NULL,                    // Content Type Length
          NULL,                    // Content Type
          NULL,                    // Content Name Length
          NULL);                   // Content Name
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    idContent.uVersion = 0;
    idContent.wszIDType = pwszContentIdType;
    idContent.wszID = pwszContentId;

    bParams.hEnablingPrincipal = hEnablingPrincipal;
    bParams.hSecureStore = NULL;
    bParams.wszRightsRequested = pwszRightsRequested;
    bParams.wszRightsGroup = SZ_MAIN_RIGHTS_GROUP;
    bParams.idResource = idContent;
    bParams.wszDefaultEnablingPrincipalCredentials = NULL;
    bParams.cAuthenticatorCount = 0;

    hr = DRMCreateBoundLicense(
        hEnv,                      // Environment handle
        &bParams,                  // Additional license options
        pwszUseLicense,            // Use license
        phBoundLicense,            // Bound license handle
        NULL);                     // Reserved

e_Exit:
    if (NULL != hEnablingPrincipal)
    {
        DRMCloseHandle(hEnablingPrincipal);
    }
    if (NULL != pwszContentId)
    {
        delete [] pwszContentId;
    }
    if (NULL != pwszContentIdType)
    {
        delete [] pwszContentIdType;
    }

    return hr;
}

/////////////////////////////////////////////////////////////////////
// The PerformCbcEncryption function performs CBC encryption on the
// given unencrypted data buffer and returns the encrypted data
// in a single, freshly allocated buffer. In practice, you may want
// to modify this function so that larger amounts of data are
// streamed in, rather than having the entire block processed (and
// memory allocated) all at once.
//
// Arguments:
//        pbDataToEncrypt         - [in]  Buffer containing the data
//                                        that is to be encrypted
//        uiUnencryptedDataLength - [in]  Length of the unencrypted
//                                        data (in bytes)
//        hEnv                    - [in]  Environment handle
//        hIssuanceLicense        - [in]  Handle to an issuance
//                                        license
//        pwszCLC                 - [in]  CLC of the publishing user
//        pwszRac                 - [in]  RAC of the publishing user
//        ppbEncryptedData        - [out] Buffer holding the newly
//                                        encrypted data
//        puiEncryptedDataLength  - [out] Length of the encrypted
//                                        data (in bytes)
HRESULT PerformCbcEncryption(__in BYTE* pbDataToEncrypt,
                             __in UINT uiUnencryptedDataLength,
                             __in DRMENVHANDLE hEnv,
                             __in DRMPUBHANDLE hIssuanceLicense,
                             __in PWSTR pwszCLC,
                             __in PWCHAR pwszRac,
                             __out PBYTE* ppbEncryptedData,
                             __out UINT* puiEncryptedDataLength)
{
    HRESULT hr = S_OK;              // Return code
    DRM_CONTEXT context;            // To hold callback information
    DWORD dwWaitResult = 0;         // Result of wait operation
    PWSTR pwszOwnerLicense = NULL;  // Owner use license
    UINT uiOwnerLicenseLength = 0;  // Size of the owner license
    DRMHANDLE hBoundLicense = NULL; // Bound license handle
    DRMHANDLE hEBEncryptor = NULL;  // Encryptor handle
    UINT uiBlockSize = 0;           // Size of each block to be
                                    // passed to DRMEncrypt
    UINT uiBlockSizeInfo = 0;       // Size of the uiBlockSize
                                    // variable
    DRMENCODINGTYPE encodingType;   // Encoding type for DRMGetInfo
    UINT uiPaddingSize = 0;         // Length of padding needed to
                                    // match block size
    UINT uiOffset = 0;              // Offset in encryption buffer

    // For our example, we will be using the "EDIT" right
    // during encryption
    const PWSTR pwszRightsRequested = SZ_EDIT_RIGHT;

    // Validate parameters
    if ((NULL == pbDataToEncrypt)
        || (NULL == hEnv)
        || (NULL == hIssuanceLicense)
        || (NULL == pwszCLC)
        || (NULL == pwszRac)
        || (NULL == ppbEncryptedData)
        || (NULL == puiEncryptedDataLength))
    {
        hr = E_INVALIDARG;
        goto e_Exit;
    }

    // Create an event for the callback function
    context.hEvent = ::CreateEvent(NULL, FALSE, FALSE, NULL);
    if (NULL == context.hEvent)
    {
        hr = HRESULT_FROM_WIN32(::GetLastError());
        goto e_Exit;
    }
    context.wszData = NULL;

    hr = DRMGetSignedIssuanceLicense(
        hEnv,                         // Environment handle
        hIssuanceLicense,             // Issuance license handle
        (DRM_SIGN_OFFLINE             // Sign offline with a CLC
            | DRM_AUTO_GENERATE_KEY), // Generate a content key
        NULL,                         // No symmetric key specified
        0,                            // No length specified
        SZ_CBC_KEY_TYPE,              // CBC encryption key type
        pwszCLC,                      // Client licensor certificate
        &StatusCallback,              // Callback function
        NULL,                         // No licensing URL specified
        (void*)&context);             // Callback context parameter
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Wait for callback to return
    dwWaitResult = ::WaitForSingleObject(context.hEvent,
                                         DW_WAIT_TIME);
    if (WAIT_OBJECT_0 != dwWaitResult)
    {
        hr = HRESULT_FROM_WIN32(::GetLastError());
        goto e_Exit;
    }
    else if (FAILED(context.hr))
    {
        hr = context.hr;
        goto e_Exit;
    }

    // Obtain the length of the owner license
    hr = DRMGetOwnerLicense(
        hIssuanceLicense,             // Issuance license handle
        &uiOwnerLicenseLength,        // Length of owner license
        NULL);                        // Query for license length
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    pwszOwnerLicense = new WCHAR[uiOwnerLicenseLength];
    if (NULL == pwszOwnerLicense)
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    hr = DRMGetOwnerLicense(
        hIssuanceLicense,             // Issuance license handle
        &uiOwnerLicenseLength,        // Length of owner license
        pwszOwnerLicense);            // Owner use license
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Proceed normally (as you would for non-CBC encryption) to
    // obtain the bound license
    hr = GetBoundLicense(hEnv,
                         pwszRac,
                         pwszOwnerLicense,
                         pwszRightsRequested,
                         hIssuanceLicense,
                         &hBoundLicense);
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    hr = DRMCreateEnablingBitsEncryptor(
        hBoundLicense,                // Bound license handle
        pwszRightsRequested,          // Requested rights
        NULL,                         // Reserved
        NULL,                         // Reserved
        &hEBEncryptor);               // Encryptor handle
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Determine the block size you need to pass to DRMEncrypt
    uiBlockSizeInfo = sizeof(uiBlockSize);
    hr = DRMGetInfo(
        hEBEncryptor,                 // Encryptor handle
        g_wszQUERY_BLOCKSIZE,         // Queried attribute
        &encodingType,                // Type of encoding to apply
        &uiBlockSizeInfo,             // Size of uiBlockSize variable
        (BYTE*)&uiBlockSize);         // Block size to use
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Since the amount of data we encrypt must be a multiple of the
    // block size, we must determine the amount of padding we need
    // to add to our data and create a buffer of the appropriate
    // size (the size of our original data + padding)
    uiPaddingSize
        = uiBlockSize - (uiUnencryptedDataLength % uiBlockSize);
    *puiEncryptedDataLength
        = uiUnencryptedDataLength + uiPaddingSize;

    *ppbEncryptedData = new BYTE[*puiEncryptedDataLength];
    if (NULL == *ppbEncryptedData)
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    // Fill the padding area with zeros
    ::SecureZeroMemory((*ppbEncryptedData + uiUnencryptedDataLength),
                       uiPaddingSize);

    // In this example, we are encrypting our content with one call
    // to DRMEncrypt for each 4 KB block (4096 bytes). In practice,
    // you may want to reduce the number of calls by passing in
    // a quantity of data that is some larger multiple of 4096 bytes.
    for (int i = 0;
         ((UINT)i * uiBlockSize) < *puiEncryptedDataLength;
         i++)
    {
        UINT uiNumBytesEncrypted = 0;
        UINT uiBufferPosition = (i * uiBlockSize);

        hr = DRMEncrypt(
            // Encryptor handle
            hEBEncryptor,
            // Starting block number (1 block = uiBlockSize)
            i,
            // Number of bytes to encrypt
            uiBlockSize,
            // Starting location of bytes to encrypt
            (pbDataToEncrypt + uiBufferPosition),
            // Number of bytes encrypted
            &uiNumBytesEncrypted,
            // Starting location for encrypted content
            (*ppbEncryptedData + uiOffset));
        if (FAILED(hr))
        {
            goto e_Exit;
        }

        uiOffset += uiNumBytesEncrypted;
    }

e_Exit:
    if (NULL != context.hEvent)
    {
        ::CloseHandle(context.hEvent);
    }
    if (NULL != context.wszData)
    {
        delete [] context.wszData;
    }
    if (NULL != pwszOwnerLicense)
    {
        delete [] pwszOwnerLicense;
    }
    if (NULL != hBoundLicense)
    {
        DRMCloseHandle(hBoundLicense);
    }
    if (NULL != hEBEncryptor)
    {
        DRMCloseHandle(hEBEncryptor);
    }

    return hr;
}

/////////////////////////////////////////////////////////////////////
// The PerformCbcDecryption function performs decryption on the
// given CBC encrypted data buffer and returns the decrypted data
// in a single freshly allocated buffer. In practice, you may want
// to modify this function so that larger quantities of data are
// streamed in, rather than having the entire block processed (and
// memory allocated) all at once.
// Arguments:
//        pbEncryptedData         - [in]  Buffer containing the data
//                                        that is to be decrypted
//        uiEncryptedDataLength   - [in]  Length of the encrypted
//                                        data (in bytes)
//        hEnv                    - [in]  Environment handle
//        hIssuanceLicense        - [in]  Handle to an issuance
//                                        license
//        pwszUseLicense          - [in]  Use license
//        pwszRac                 - [in]  RAC of the publishing user
//        ppbDecryptedData        - [out] Buffer holding the newly
//                                        decrypted data
HRESULT PerformCbcDecryption(__in BYTE* pbEncryptedData,
                             __in UINT uiEncryptedDataLength,
                             __in DRMENVHANDLE hEnv,
                             __in DRMPUBHANDLE hIssuanceLicense,
                             __in PWSTR pwszUseLicense,
                             __in PWCHAR pwszRac,
                             __out PBYTE* ppbDecryptedData)
{
    HRESULT hr = S_OK;              // Return code
    DRMHANDLE hBoundLicense = NULL; // Bound license handle
    DRMHANDLE hEBDecryptor = NULL;  // Decryptor handle
    PWSTR pwszKeyType = NULL;       // Key type used
    UINT uiKeyTypeLength = 0;       // Length of pwszKeyType
    UINT uiBlockSize = 0;           // Size of each block to be
                                    // passed to DRMEncrypt
    UINT uiBlockSizeInfo = 0;       // Size of the uiBlockSize
                                    // variable
    DRMENCODINGTYPE encodingType;   // Encoding type for DRMGetInfo
    UINT uiPaddingSize = 0;         // Length of padding needed to
                                    // match block size
    UINT uiOffset = 0;              // Offset in encryption buffer

    // For the example, the "VIEW" right is used
    // during decryption
    const PWSTR pwszRightsRequested = SZ_VIEW_RIGHT;

    // Validate parameters
    if ((NULL == pbEncryptedData)
        || (NULL == hEnv)
        || (NULL == hIssuanceLicense)
        || (NULL == pwszUseLicense)
        || (NULL == pwszRac)
        || (NULL == ppbDecryptedData))
    {
        hr = E_INVALIDARG;
        goto e_Exit;
    }

    // Proceed normally (as you would for non-CBC decryption) to
    // obtain the bound license
    hr = GetBoundLicense(hEnv,
                         pwszRac,
                         pwszUseLicense,
                         pwszRightsRequested,
                         hIssuanceLicense,
                         &hBoundLicense);
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    hr = DRMCreateEnablingBitsDecryptor(
        hBoundLicense,                // Bound license handle
        pwszRightsRequested,          // Requested rights
        NULL,                         // Reserved
        NULL,                         // Reserved
        &hEBDecryptor);               // Decryptor handle
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    // Verify/Determine that CBC decryption is needed. In practice,
    // this may not be needed if you already know whether or not
    // the cipher mode used is CBC
    hr = DRMGetInfo(
        hEBDecryptor,                 // Decryptor handle
        g_wszQUERY_SYMMETRICKEYTYPE,  // Queried attribute
        &encodingType,                // Type of encoding to apply
        &uiKeyTypeLength,             // Size of key type variable
        NULL);                        // Query for length
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    pwszKeyType = new WCHAR[uiKeyTypeLength];
    if (NULL == pwszKeyType)
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    hr = DRMGetInfo(
        hEBDecryptor,                 // Decryptor handle
        g_wszQUERY_SYMMETRICKEYTYPE,  // Queried attribute
        &encodingType,                // Type of encoding to apply
        &uiKeyTypeLength,             // Size of key type variable
        (BYTE*)pwszKeyType);          // Key type used
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    if (!wcscmp(SZ_CBC_KEY_TYPE, pwszKeyType))
    {
        // Unexpected -- in practice, you may want to instead
        // handle decryption for this non-CBC key type
        hr = E_UNEXPECTED;
        goto e_Exit;
    }

    // Verify/Determine the block size you need to pass to DRMDecrypt
    uiBlockSizeInfo = sizeof(uiBlockSize);
    hr = DRMGetInfo(
        hEBDecryptor,                 // Decryptor handle
        g_wszQUERY_BLOCKSIZE,         // Queried attribute
        &encodingType,                // Type of encoding to apply
        &uiBlockSizeInfo,             // Size of uiBlockSize variable
        (BYTE*)&uiBlockSize);         // Block size to use
    if (FAILED(hr))
    {
        goto e_Exit;
    }

    *ppbDecryptedData = new BYTE[uiEncryptedDataLength];
    if (NULL == *ppbDecryptedData)
    {
        hr = E_OUTOFMEMORY;
        goto e_Exit;
    }

    // In this example, the content is being decrypted with one call
    // to DRMDecrypt for each 4 KB block (4096 bytes). In practice,
    // you may want to reduce the number of calls by passing in
    // a quantity of data that is some larger multiple of 4096 bytes.
    for (int i = 0;
         ((UINT)i * uiBlockSize) < uiEncryptedDataLength;
         i++)
    {
        UINT uiNumBytesDecrypted = 0;
        UINT uiBufferPosition = (i * uiBlockSize);

        hr = DRMDecrypt(
            // Decryptor handle
            hEBDecryptor,
            // Starting block number (1 block = uiBlockSize)
            i,
            // Number of bytes to decrypt
            uiBlockSize,
            // Starting location of bytes to decrypt
            (pbEncryptedData + uiBufferPosition),
            // Number of bytes decrypted
            &uiNumBytesDecrypted,
            // Starting location for decrypted content
            (*ppbDecryptedData + uiOffset));
        if (FAILED(hr))
        {
            goto e_Exit;
        }

        uiOffset += uiNumBytesDecrypted;
    }

e_Exit:
    if (NULL != hBoundLicense)
    {
        DRMCloseHandle(hBoundLicense);
    }
    if (NULL != hEBDecryptor)
    {
        DRMCloseHandle(hEBDecryptor);
    }
    if (NULL != pwszKeyType)
    {
        delete [] pwszKeyType;
    }

    return hr;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsencryptor">DRMCreateEnablingBitsEncryptor</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdecrypt">DRMDecrypt</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/encrypting-content">Encrypting Content</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/encrypting-content-code-example">Encrypting Content Code Example</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/encryption-encryptcontent-cpp">Encryption_EncryptContent.cpp</a>