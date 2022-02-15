---
UID: NF:mfapi.MFCreateTempFile
title: MFCreateTempFile function (mfapi.h)
description: Creates a byte stream that is backed by a temporary local file.
helpviewer_keywords: ["1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678","MFCreateTempFile","MFCreateTempFile function [Media Foundation]","mf.mfcreatetempfile","mfapi/MFCreateTempFile"]
old-location: mf\mfcreatetempfile.htm
tech.root: mf
ms.assetid: 1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678
ms.date: 12/05/2018
ms.keywords: 1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678, MFCreateTempFile, MFCreateTempFile function [Media Foundation], mf.mfcreatetempfile, mfapi/MFCreateTempFile
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateTempFile
 - mfapi/MFCreateTempFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateTempFile
---

# MFCreateTempFile function


## -description

Creates a byte stream that is backed by a temporary local file.

## -parameters

### -param AccessMode

The requested access mode, specified as a member of the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_accessmode">MF_FILE_ACCESSMODE</a> enumeration.

### -param OpenMode

The behavior of the function if the file already exists or does not exist, specified as a member of the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_openmode">MF_FILE_OPENMODE</a> enumeration.

### -param fFlags

Bitwise <b>OR</b> of values from the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_flags">MF_FILE_FLAGS</a> enumeration.

### -param ppIByteStream

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the byte stream. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a file in the system temporary folder, and then returns a byte stream object for that file.
      The full path name of the file is stored in the <a href="/windows/desktop/medfound/mf-bytestream-origin-name-attribute">MF_BYTESTREAM_ORIGIN_NAME</a> attribute. The file is created with the <b>FILE_FLAG_DELETE_ON_CLOSE</b> flag, and is deleted after the byte stream is released.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>