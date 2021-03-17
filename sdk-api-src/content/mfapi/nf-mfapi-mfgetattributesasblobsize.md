---
UID: NF:mfapi.MFGetAttributesAsBlobSize
title: MFGetAttributesAsBlobSize function (mfapi.h)
description: Retrieves the size of the buffer needed for the MFGetAttributesAsBlob function.
helpviewer_keywords: ["52abfe30-a18d-45f7-93db-13f87b0647b7","MFGetAttributesAsBlobSize","MFGetAttributesAsBlobSize function [Media Foundation]","mf.mfgetattributesasblobsize","mfapi/MFGetAttributesAsBlobSize"]
old-location: mf\mfgetattributesasblobsize.htm
tech.root: mf
ms.assetid: 52abfe30-a18d-45f7-93db-13f87b0647b7
ms.date: 12/05/2018
ms.keywords: 52abfe30-a18d-45f7-93db-13f87b0647b7, MFGetAttributesAsBlobSize, MFGetAttributesAsBlobSize function [Media Foundation], mf.mfgetattributesasblobsize, mfapi/MFGetAttributesAsBlobSize
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
 - MFGetAttributesAsBlobSize
 - mfapi/MFGetAttributesAsBlobSize
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
 - MFGetAttributesAsBlobSize
---

# MFGetAttributesAsBlobSize function


## -description

Retrieves the size of the buffer needed for the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob">MFGetAttributesAsBlob</a> function.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param pcbBufSize [out]

Receives the required size of the array, in bytes.

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

Use this function to find the size of the array that is needed for the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob">MFGetAttributesAsBlob</a> function.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>