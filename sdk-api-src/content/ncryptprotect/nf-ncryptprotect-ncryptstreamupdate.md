---
UID: NF:ncryptprotect.NCryptStreamUpdate
title: NCryptStreamUpdate function (ncryptprotect.h)
description: Encrypts and decrypts blocks of data.
helpviewer_keywords: ["NCryptStreamUpdate","NCryptStreamUpdate function [Security]","ncryptprotect/NCryptStreamUpdate","security.ncryptstreamupdate"]
old-location: security\ncryptstreamupdate.htm
tech.root: security
ms.assetid: 417F9267-6055-489C-AF26-BEF5E17CB8B4
ms.date: 12/05/2018
ms.keywords: NCryptStreamUpdate, NCryptStreamUpdate function [Security], ncryptprotect/NCryptStreamUpdate, security.ncryptstreamupdate
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptStreamUpdate
 - ncryptprotect/NCryptStreamUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptStreamUpdate
---

# NCryptStreamUpdate function


## -description

The <b>NCryptStreamUpdate</b> function encrypts and decrypts blocks of data.

## -parameters

### -param hStream [in]

Handle to the stream object created by calling <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>.

### -param pbData [in]

Pointer to the byte array to be processed.

### -param cbData

Number of bytes in the binary array specified by the <i>pbData</i> parameter.

### -param fFinal

A Boolean value that specifies whether the last block of data has been processed.

## -returns

Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_DATA</b></dt>
</dl>
</td>
<td width="60%">
The content could not be decoded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The stream handle pointed to by the <i>hStream</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available to process the content.

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> to open a stream before calling <b>NCryptStreamUpdate</b>

Messages can be so large that processing them all at once by storing the entire message in memory can be difficult. It is possible, however,  to process large messages by partitioning the data to be processed into manageable blocks.

To do this, use <b>NCryptStreamUpdate</b> in a loop that advances through the file block by block. As the streamed message is processed, the resulting output data is passed back to your application by using a callback function that you specify. This is shown by the following example. For more information about the callback function, see  <a href="/windows/desktop/api/ncryptprotect/nc-ncryptprotect-pfncryptstreamoutputcallback">PFNCryptStreamOutputCallback</a>.

<div class="alert"><b>Note</b>  We recommend against using too small of a block size. Small blocks require more calls and therefore more calling overhead. Further, the streaming APIs are optimized for larger blocks. You should experiment to find the best block size for the data  you must process.</div>
<div> </div>

```cpp
BOOL                        fFinal = FALSE;
PBYTE                       pbBuf = NULL;

// Determine the number of bytes to read.
DWORD cbData = GetFileSize( hFileIn, NULL );

// Call NCryptStreamUpdate while there is data left to read.
while(FALSE == fFinal)
{
    // Read dwBlockSize bytes from the file.
    if(dwBlockSize > 1)
    {
        if( !ReadFile(hFileIn, pbBuf, dwBlockSize, &cbResult, NULL) )
        {
            hr = HRESULT_FROM_WIN32(hr);            
            goto CleanUp;
        }
    }

    // Decrement the number of bytes to read by the current amount read.
    cbData -= cbResult;

    // Set fFinal if there are no bytes left to read.
    if (cbData <= 0) fFinal = TRUE;

    // Encrypt (or decrypt) the bytes pointed to by pbBuf
    hr = NCryptStreamUpdate(hStream, pbBuf, cbResult, fFinal); 
    if( FAILED(hr) )
    {            
        goto CleanUp;
    }         
}      

CleanUp:
    if( NULL != hStream )
    {
        NCryptStreamClose(hStream);
    }
    if( NULL != hDescriptor )
    {
        NCryptCloseProtectionDescriptor( hDescriptor );
    }
    if(NULL != pbBuf)
    {
        LocalFree(pbBuf);
        pbBuf = NULL;
    }
```

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>