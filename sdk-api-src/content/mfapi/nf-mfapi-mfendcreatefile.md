---
UID: NF:mfapi.MFEndCreateFile
title: MFEndCreateFile function (mfapi.h)
description: Completes an asynchronous request to create a byte stream from a file.
helpviewer_keywords: ["MFEndCreateFile","MFEndCreateFile function [Media Foundation]","daa92660-5d0d-4c7c-985a-ad621eca4bfc","mf.mfendcreatefile","mfapi/MFEndCreateFile"]
old-location: mf\mfendcreatefile.htm
tech.root: mf
ms.assetid: daa92660-5d0d-4c7c-985a-ad621eca4bfc
ms.date: 12/05/2018
ms.keywords: MFEndCreateFile, MFEndCreateFile function [Media Foundation], daa92660-5d0d-4c7c-985a-ad621eca4bfc, mf.mfendcreatefile, mfapi/MFEndCreateFile
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
 - MFEndCreateFile
 - mfapi/MFEndCreateFile
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
 - MFEndCreateFile
---

# MFEndCreateFile function


## -description

Completes an asynchronous request to create a byte stream from a file.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method.

### -param ppFile [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the byte stream. The caller must release the interface.

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

Call this function when the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a> function completes asynchronously.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>