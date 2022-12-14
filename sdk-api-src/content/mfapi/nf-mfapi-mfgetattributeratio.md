---
UID: NF:mfapi.MFGetAttributeRatio
title: MFGetAttributeRatio function (mfapi.h)
description: Retrieves an attribute whose value is a ratio.
helpviewer_keywords: ["2572c30c-4ae1-42b7-b1f7-6c564d936c60","MFGetAttributeRatio","MFGetAttributeRatio function [Media Foundation]","mf.mfgetattributeratio","mfapi/MFGetAttributeRatio"]
old-location: mf\mfgetattributeratio.htm
tech.root: mf
ms.assetid: 2572c30c-4ae1-42b7-b1f7-6c564d936c60
ms.date: 12/05/2018
ms.keywords: 2572c30c-4ae1-42b7-b1f7-6c564d936c60, MFGetAttributeRatio, MFGetAttributeRatio function [Media Foundation], mf.mfgetattributeratio, mfapi/MFGetAttributeRatio
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
 - MFGetAttributeRatio
 - mfapi/MFGetAttributeRatio
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
 - MFGetAttributeRatio
---

# MFGetAttributeRatio function


## -description

Retrieves an attribute whose value is a ratio.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

<b>GUID</b> that identifies which value to retrieve. The attribute type must be MF_ATTRIBUTE_UINT64.

### -param punNumerator [out]

Receives the numerator of the ratio.

### -param punDenominator [out]

Receives the denominator of the ratio.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Some attributes specify a ratio as a packed <b>UINT64</b> value. Use this function to get the numerator and denominator as separate 32-bit values.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio">MFSetAttributeRatio</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>