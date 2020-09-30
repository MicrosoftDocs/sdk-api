---
UID: NF:dmort.MoCopyMediaType
title: MoCopyMediaType function (dmort.h)
description: The MoCopyMediaType function copies the members of one media type structure into another media type structure.
helpviewer_keywords: ["MoCopyMediaType","MoCopyMediaType function [DirectShow]","dmort/MoCopyMediaType","dshow.mocopymediatype"]
old-location: dshow\mocopymediatype.htm
tech.root: dshow
ms.assetid: 7b6325bf-a996-467e-896d-a6dc41f63fd4
ms.date: 12/05/2018
ms.keywords: MoCopyMediaType, MoCopyMediaType function [DirectShow], dmort/MoCopyMediaType, dshow.mocopymediatype
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
 - MoCopyMediaType
 - dmort/MoCopyMediaType
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
 - MoCopyMediaType
---

# MoCopyMediaType function


## -description

The <b>MoCopyMediaType</b> function copies the members of one media type structure into another media type structure.

## -parameters

### -param pmtDest

Pointer to the target <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure. The caller must allocate, but not initialize, this structure.

### -param pmtSrc

Pointer to the source <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure.

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

This function copies all the members of <i>pmtSrc</i> to <i>pmtDest</i> and copies the format block. The caller must free the target media type by calling the <a href="/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> function.