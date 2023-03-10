---
UID: NF:mfapi.MFGetAttribute2UINT32asUINT64
title: MFGetAttribute2UINT32asUINT64 function (mfapi.h)
description: Gets an attribute whose value is two UINT32 values packed into a UINT64.
helpviewer_keywords: ["MFGetAttribute2UINT32asUINT64","MFGetAttribute2UINT32asUINT64 function [Media Foundation]","mf.mfgetattribute2uint32asuint64","mfobjects/MFGetAttribute2UINT32asUINT64"]
old-location: mf\mfgetattribute2uint32asuint64.htm
tech.root: mf
ms.assetid: 2b3050da-6914-4d7f-af6f-d8e504da0870
ms.date: 12/05/2018
ms.keywords: MFGetAttribute2UINT32asUINT64, MFGetAttribute2UINT32asUINT64 function [Media Foundation], mf.mfgetattribute2uint32asuint64, mfobjects/MFGetAttribute2UINT32asUINT64
req.header: mfapi.h
req.include-header: Mfapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetAttribute2UINT32asUINT64
 - mfapi/MFGetAttribute2UINT32asUINT64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFGetAttribute2UINT32asUINT64
---

# MFGetAttribute2UINT32asUINT64 function


## -description

Gets an attribute whose value is two <b>UINT32</b> values packed into a <b>UINT64</b>.

## -parameters

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

A <b>GUID</b> that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT64</b>.

### -param punHigh32 [out]

Receives the high-order 32 bits.

### -param punLow32 [out]

Receives the low-order 32 bits.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a <b>UINT64</b>.
              

</td>
</tr>
</table>

## -remarks

Internally, this function calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a> to get the <b>UINT64</b> value, and <a href="/windows/desktop/api/mfapi/nf-mfapi-unpack2uint32asuint64">Unpack2UINT32AsUINT64</a> to unpack the two 32-bit values.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>