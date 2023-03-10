---
UID: NF:msdrm.DRMDecrypt
title: DRMDecrypt function (msdrm.h)
description: Decrypts encrypted content.
helpviewer_keywords: ["DRMDecrypt","DRMDecrypt function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDecrypt","rm.drmdecrypt"]
old-location: rm\drmdecrypt.htm
tech.root: rm
ms.assetid: 8e0cb353-4670-4cf7-bcd8-81ebd0adfe32
ms.date: 12/05/2018
ms.keywords: DRMDecrypt, DRMDecrypt function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDecrypt, rm.drmdecrypt
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
 - DRMDecrypt
 - msdrm/DRMDecrypt
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
 - DRMDecrypt
---

# DRMDecrypt function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDecrypt</b> function decrypts encrypted content.

## -parameters

### -param hCryptoProvider [in]

A handle to an AD RMS decrypting object created by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsdecryptor">DRMCreateEnablingBitsDecryptor</a>.

### -param iPosition [in]

Position in the buffer at which to start decrypting. <b>0</b> corresponds to the first block in a buffer, <b>1</b> corresponds to the second block, and so on. See the example later in this topic.

### -param cNumInBytes [in]

Number of bytes to decrypt.

### -param pbInData [in]

Pointer to a buffer that contains the bytes to decrypt.

### -param pcNumOutBytes [in, out]

Size, in bytes,  of the decrypted data.

### -param pbOutData [out]

Decrypted data.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Memory allocation and release of the decrypted content is the responsibility of the calling function. The following code sample, from <a href="/previous-versions/windows/desktop/adrms_sdk/decrypting-content">Decrypting Content</a>, shows how to decrypt content in blocks. This particular example already knows the size of the content to decrypt and allocates memory beforehand. If you must determine the number of bytes to allocate, however,  the required buffer size is returned in the <i>pcNumOutBytes</i> parameter after the first call. Allocate memory and call the function again with  <i>pbOutData</i> set to point to the new memory.


```cpp
#include "DecryptingContent.h"

/*===================================================================
File:      Decryption_DecryptContent.cpp

THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.
===================================================================*/

/////////////////////////////////////////////////////////////////////
// The DecryptContent function decrypts content. The content to be 
// decrypted was created by the EncryptingContent example shown 
// earlier in this documentation.
//
HRESULT DecryptContent(
          DRMHANDLE      hBoundLic,
          UINT           uiEncrypted,
          BYTE*          pbEncrypted,
          BYTE**         ppbDecrypted)
{
  HRESULT hr = S_OK;                  // HRESULT return code
  UINT uiBlock = 0;                   // Decryption block size (16)
  UINT uiBytes = 0;                   // Size of uiBlock variable (4)
  UINT uiDecrypted = 0;               // Number of decrypted bytes
  UINT uiOffset = 0;                  // Decryption buffer offset
  DRMHANDLE hEBDecryptor = NULL;      // Decrypting object handle
  DRMENCODINGTYPE eType;

  wprintf(L"\r\nEntering DecryptContent.\r\n");

  // Validate the input parameters.
  if ( NULL==hBoundLic ||
       NULL==pbEncrypted ||
       NULL==ppbDecrypted)
       return E_INVALIDARG;

  // Create a decrypting object.
  hr = DRMCreateEnablingBitsDecryptor( 
          hBoundLic,                // Bound license handle
          L"EDIT",                  // Requested right
          NULL,                     // Reserved
          NULL,                     // Reserved
          &hEBDecryptor);           // Decrypting object pointer
  if (FAILED(hr)) goto e_Exit;
  wprintf(L"DRMCreateEnablingBitsDecryptor: hEBDecryptor = %i\r\n",
          hEBDecryptor);

  // Retrieve the size, in bytes, of the memory block that must 
  // be passed to DRMDecrypt.
  uiBytes= sizeof(uiBlock);
  hr = DRMGetInfo(
          hEBDecryptor,               // Decrypting object handle
          g_wszQUERY_BLOCKSIZE,       // Attribute to query for
          &eType,                     // Type of encoding to apply
          &uiBytes,                   // Size of uiBlock variable
          (BYTE*)&uiBlock);           // Size of memory block
  if(FAILED(hr)) goto e_Exit;
  wprintf(L"DRMGetInfo: uiBlock = %u\r\n", uiBlock);

  // Allocate memory for the decrypted content.
  // Note: This example uses a buffer of known size to store the
  //       decrypted content.  Typically, however, the buffer to 
  //       store the content should be allocated based on the size
  //       returned by the first call to DRMDecrypt.
  *ppbDecrypted = new BYTE[uiEncrypted];
  if (NULL == *ppbDecrypted)
  {
    hr = E_OUTOFMEMORY;
    goto e_Exit;
  }

  // Decrypt the content.
  for ( int j = 0; (UINT)j * uiBlock < uiEncrypted; j++ )
  {
    hr = DRMDecrypt( 
          hEBDecryptor,               // Decrypting object handle
          j * uiBlock,                // Position in the buffer
          uiBlock,                    // Number of bytes to decrypt
          pbEncrypted + (j*uiBlock),  // Bytes to decrypt
          &uiDecrypted,               // Number of decrypted bytes
          NULL);                      // Set to NULL on first call
    if(FAILED(hr)) goto e_Exit;

    hr = DRMDecrypt( 
          hEBDecryptor,               // Decrypting object handle
          j * uiBlock,                // Position in the buffer 
          uiBlock,                    // Number of bytes to decrypt
          pbEncrypted + (j*uiBlock),  // Bytes to decrypt
          &uiDecrypted,               // Number of decrypted bytes
          *ppbDecrypted + uiOffset);  // Decrypted data
    if(FAILED(hr)) goto e_Exit;

    uiOffset += uiDecrypted;          // Increment the buffer offset
  }

e_Exit:

  if (NULL != hEBDecryptor)
  {
    hr = DRMCloseHandle(hEBDecryptor);
    hEBDecryptor = NULL;
  }
  
  wprintf(L"Leaving DecryptContent: hr = %x\r\n", hr);
  return hr;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsdecryptor">DRMCreateEnablingBitsDecryptor</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmencrypt">DRMEncrypt</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetinfo">DRMGetInfo</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decrypting-content">Decrypting Content</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decrypting-content-code-example">Decrypting Content Code Example</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decryption-decryptcontent-cpp">Decryption_DecryptContent.cpp</a>