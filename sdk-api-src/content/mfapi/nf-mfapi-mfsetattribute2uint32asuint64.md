---
UID: NF:mfapi.MFSetAttribute2UINT32asUINT64
title: MFSetAttribute2UINT32asUINT64 function (mfapi.h)
description: Packs two UINT32 values into a UINT64 attribute value.
helpviewer_keywords: ["MFSetAttribute2UINT32asUINT64","MFSetAttribute2UINT32asUINT64 function [Media Foundation]","mf.mfsetattribute2uint32asuint64","mfobjects/MFSetAttribute2UINT32asUINT64"]
old-location: mf\mfsetattribute2uint32asuint64.htm
tech.root: mf
ms.assetid: a9c64e49-e249-49ce-8d58-109a7f247fe9
ms.date: 12/05/2018
ms.keywords: MFSetAttribute2UINT32asUINT64, MFSetAttribute2UINT32asUINT64 function [Media Foundation], mf.mfsetattribute2uint32asuint64, mfobjects/MFSetAttribute2UINT32asUINT64
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
 - MFSetAttribute2UINT32asUINT64
 - mfapi/MFSetAttribute2UINT32asUINT64
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
 - MFSetAttribute2UINT32asUINT64
---

# MFSetAttribute2UINT32asUINT64 function


## -description

Packs two <b>UINT32</b> values into a <b>UINT64</b> attribute value.

## -parameters

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

A <b>GUID</b> that identifies the value to set. If this key already exists, the function overwrites the old value.

### -param unHigh32 [in]

The value to store in the high-order 32 bits of the <b>UINT64</b> value.

### -param unLow32 [in]

The value to store in the low-order 32 bits of the <b>UINT64</b> value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Internally, this functions calls <a href="/windows/desktop/api/mfapi/nf-mfapi-pack2uint32asuint64">Pack2UINT32AsUINT64</a> to create the 64-bit value, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64">IMFAttributes::SetUINT64</a> to set the attribute.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>