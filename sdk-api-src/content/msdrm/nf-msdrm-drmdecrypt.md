---
UID: NF:msdrm.DRMDecrypt
title: DRMDecrypt function
author: windows-sdk-content
description: Decrypts encrypted content.
old-location: rm\drmdecrypt.htm
tech.root: AdRms_Sdk
ms.assetid: 8e0cb353-4670-4cf7-bcd8-81ebd0adfe32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRMDecrypt, DRMDecrypt function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDecrypt, rm.drmdecrypt
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMDecrypt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDecrypt function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDecrypt</b> function decrypts encrypted content.


## -parameters




### -param hCryptoProvider [in]

A handle to an AD RMS decrypting object created by <a href="https://msdn.microsoft.com/133582e2-6396-476f-a28b-37ed0257fb79">DRMCreateEnablingBitsDecryptor</a>.


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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Memory allocation and release of the decrypted content is the responsibility of the calling function. The following code sample, from <a href="https://msdn.microsoft.com/768767a0-b76c-4a9a-a4b1-22dd1923c667">Decrypting Content</a>, shows how to decrypt content in blocks. This particular example already knows the size of the content to decrypt and allocates memory beforehand. If you must determine the number of bytes to allocate, however,  the required buffer size is returned in the <i>pcNumOutBytes</i> parameter after the first call. Allocate memory and call the function again with  <i>pbOutData</i> set to point to the new memory.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include "DecryptingContent.h"

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
          &amp;hEBDecryptor);           // Decrypting object pointer
  if (FAILED(hr)) goto e_Exit;
  wprintf(L"DRMCreateEnablingBitsDecryptor: hEBDecryptor = %i\r\n",
          hEBDecryptor);

  // Retrieve the size, in bytes, of the memory block that must 
  // be passed to DRMDecrypt.
  uiBytes= sizeof(uiBlock);
  hr = DRMGetInfo(
          hEBDecryptor,               // Decrypting object handle
          g_wszQUERY_BLOCKSIZE,       // Attribute to query for
          &amp;eType,                     // Type of encoding to apply
          &amp;uiBytes,                   // Size of uiBlock variable
          (BYTE*)&amp;uiBlock);           // Size of memory block
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
  for ( int j = 0; (UINT)j * uiBlock &lt; uiEncrypted; j++ )
  {
    hr = DRMDecrypt( 
          hEBDecryptor,               // Decrypting object handle
          j * uiBlock,                // Position in the buffer
          uiBlock,                    // Number of bytes to decrypt
          pbEncrypted + (j*uiBlock),  // Bytes to decrypt
          &amp;uiDecrypted,               // Number of decrypted bytes
          NULL);                      // Set to NULL on first call
    if(FAILED(hr)) goto e_Exit;

    hr = DRMDecrypt( 
          hEBDecryptor,               // Decrypting object handle
          j * uiBlock,                // Position in the buffer 
          uiBlock,                    // Number of bytes to decrypt
          pbEncrypted + (j*uiBlock),  // Bytes to decrypt
          &amp;uiDecrypted,               // Number of decrypted bytes
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/133582e2-6396-476f-a28b-37ed0257fb79">DRMCreateEnablingBitsDecryptor</a>



<a href="https://msdn.microsoft.com/1de19409-2b14-4ab0-9853-23ee5741a7ae">DRMEncrypt</a>



<a href="https://msdn.microsoft.com/6cb1275a-c0e4-48df-a389-76add74bdabd">DRMGetInfo</a>



<a href="https://msdn.microsoft.com/768767a0-b76c-4a9a-a4b1-22dd1923c667">Decrypting Content</a>



<a href="https://msdn.microsoft.com/f4e3da83-2b6b-4975-898c-ed3d5e6c45ff">Decrypting Content Code Example</a>



<a href="https://msdn.microsoft.com/3804216c-6698-43f0-9077-35149704375a">Decryption_DecryptContent.cpp</a>
 

 

