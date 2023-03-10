---
UID: NF:mfapi.MFBeginCreateFile
title: MFBeginCreateFile function (mfapi.h)
description: Begins an asynchronous request to create a byte stream from a file.
helpviewer_keywords: ["MFBeginCreateFile","MFBeginCreateFile function [Media Foundation]","aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd","mf.mfbegincreatefile","mfapi/MFBeginCreateFile"]
old-location: mf\mfbegincreatefile.htm
tech.root: mf
ms.assetid: aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd
ms.date: 12/05/2018
ms.keywords: MFBeginCreateFile, MFBeginCreateFile function [Media Foundation], aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd, mf.mfbegincreatefile, mfapi/MFBeginCreateFile
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
 - MFBeginCreateFile
 - mfapi/MFBeginCreateFile
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
 - MFBeginCreateFile
---

# MFBeginCreateFile function


## -description

Begins an asynchronous request to create a byte stream from a file.

## -parameters

### -param AccessMode [in]

The requested access mode, specified as a member of the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_accessmode">MF_FILE_ACCESSMODE</a> enumeration.

### -param OpenMode [in]

The behavior of the function if the file already exists or does not exist, specified as a member of the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_openmode">MF_FILE_OPENMODE</a> enumeration.

### -param fFlags [in]

Bitwise <b>OR</b> of values from the <a href="/windows/win32/api/mfobjects/ne-mfobjects-mf_file_flags">MF_FILE_FLAGS</a> enumeration.

### -param pwszFilePath [in]

Pointer to a null-terminated string containing the file name.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface

### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

### -param ppCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcancelcreatefile">MFCancelCreateFile</a> function. The caller must release the interface. This parameter is optional and can be <b>NULL</b>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

When the request is completed, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. The callback object should then call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfendcreatefile">MFEndCreateFile</a> function to get a pointer to the byte stream.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>