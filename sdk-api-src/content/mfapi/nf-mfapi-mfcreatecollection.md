---
UID: NF:mfapi.MFCreateCollection
title: MFCreateCollection function (mfapi.h)
description: Creates an empty collection object.
helpviewer_keywords: ["6a7bf7b6-62f1-4eac-9849-39021ee50f42","MFCreateCollection","MFCreateCollection function [Media Foundation]","mf.mfcreatecollection","mfapi/MFCreateCollection"]
old-location: mf\mfcreatecollection.htm
tech.root: mf
ms.assetid: 6a7bf7b6-62f1-4eac-9849-39021ee50f42
ms.date: 12/05/2018
ms.keywords: 6a7bf7b6-62f1-4eac-9849-39021ee50f42, MFCreateCollection, MFCreateCollection function [Media Foundation], mf.mfcreatecollection, mfapi/MFCreateCollection
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateCollection
 - mfapi/MFCreateCollection
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
 - MFCreateCollection
---

# MFCreateCollection function


## -description

Creates an empty collection object.

## -parameters

### -param ppIMFCollection [out]

Receives a pointer to the collection object's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a> interface. The caller must release the interface.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>