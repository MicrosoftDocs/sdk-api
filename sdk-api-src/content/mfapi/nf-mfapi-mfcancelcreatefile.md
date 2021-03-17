---
UID: NF:mfapi.MFCancelCreateFile
title: MFCancelCreateFile function (mfapi.h)
description: Cancels an asynchronous request to create a byte stream from a file.
helpviewer_keywords: ["MFCancelCreateFile","MFCancelCreateFile function [Media Foundation]","b3c0cad8-d578-4752-a2ea-0aa5c35a181a","mf.mfcancelcreatefile","mfapi/MFCancelCreateFile"]
old-location: mf\mfcancelcreatefile.htm
tech.root: mf
ms.assetid: b3c0cad8-d578-4752-a2ea-0aa5c35a181a
ms.date: 12/05/2018
ms.keywords: MFCancelCreateFile, MFCancelCreateFile function [Media Foundation], b3c0cad8-d578-4752-a2ea-0aa5c35a181a, mf.mfcancelcreatefile, mfapi/MFCancelCreateFile
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
 - MFCancelCreateFile
 - mfapi/MFCancelCreateFile
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
 - MFCancelCreateFile
---

# MFCancelCreateFile function


## -description

Cancels an asynchronous request to create a byte stream from a file.

## -parameters

### -param pCancelCookie [in]

A pointer to the <b>IUnknown</b> interface of the cancellation object. This pointer is received in the <i>ppCancelCookie</i> parameter of the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a> function.

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

You can use this function to cancel a previous call to <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>. Because that function is asynchronous, however, it might complete before the operation can be canceled. Therefore, your callback might still be invoked after you call this function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>