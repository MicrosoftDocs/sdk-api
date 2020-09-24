---
UID: NF:dmort.MoDuplicateMediaType
title: MoDuplicateMediaType function (dmort.h)
description: The MoDuplicateMediaType function duplicates a media type structure.
helpviewer_keywords: ["MoDuplicateMediaType","MoDuplicateMediaType function [DirectShow]","dmort/MoDuplicateMediaType","dshow.moduplicatemediatype"]
old-location: dshow\moduplicatemediatype.htm
tech.root: dshow
ms.assetid: 8804ec3f-98c7-4305-a02c-67f5e560b4f7
ms.date: 12/05/2018
ms.keywords: MoDuplicateMediaType, MoDuplicateMediaType function [DirectShow], dmort/MoDuplicateMediaType, dshow.moduplicatemediatype
req.header: dmort.h
req.include-header: Dmo.h
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MoDuplicateMediaType
 - dmort/MoDuplicateMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - MoDuplicateMediaType
---

# MoDuplicateMediaType function


## -description

The <b>MoDuplicateMediaType</b> function duplicates a media type structure.

## -parameters

### -param ppmtDest

Address of a pointer to a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure that receives the duplicated structure.

### -param pmtSrc

Pointer to the media type structure to duplicate.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

This method is equivalent to calling <a href="/windows/desktop/api/dmort/nf-dmort-mocreatemediatype">MoCreateMediaType</a> and <a href="/windows/desktop/api/dmort/nf-dmort-mocopymediatype">MoCopyMediaType</a>. The caller must delete the returned media type structure by calling the <a href="/windows/desktop/api/dmort/nf-dmort-modeletemediatype">MoDeleteMediaType</a> function.