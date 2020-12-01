---
UID: NF:mfapi.MFGetAttributeUINT64
title: MFGetAttributeUINT64 function (mfapi.h)
description: Returns a UINT64 value from an attribute store, or a default value if the attribute is not present.
helpviewer_keywords: ["843946a4-d270-4440-9818-59e95cbf9a5b","MFGetAttributeUINT64","MFGetAttributeUINT64 function [Media Foundation]","mf.mfgetattributeuint64","mfapi/MFGetAttributeUINT64"]
old-location: mf\mfgetattributeuint64.htm
tech.root: mf
ms.assetid: 843946a4-d270-4440-9818-59e95cbf9a5b
ms.date: 12/05/2018
ms.keywords: 843946a4-d270-4440-9818-59e95cbf9a5b, MFGetAttributeUINT64, MFGetAttributeUINT64 function [Media Foundation], mf.mfgetattributeuint64, mfapi/MFGetAttributeUINT64
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetAttributeUINT64
 - mfapi/MFGetAttributeUINT64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFGetAttributeUINT64
---

# MFGetAttributeUINT64 function


## -description

Returns a <b>UINT64</b> value from an attribute store, or a default value if the attribute is not present.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

GUID that identifies which value to retrieve.

### -param unDefault [in]

Default value to return if the attribute store does not contain the specified attribute.

## -returns

Returns a <b>UINT64</b> value.

## -remarks

This helper function queries the attribute store for the <b>UINT64</b> value specified by guidKey. If the value is not present, the function returns <i>unDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a> and check for MF_E_ATTRIBUTENOTFOUND.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>