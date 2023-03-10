---
UID: NF:mfapi.MFGetAttributeSize
title: MFGetAttributeSize function (mfapi.h)
description: Retrieves an attribute whose value is a size, expressed as a width and height.
helpviewer_keywords: ["MFGetAttributeSize","MFGetAttributeSize function [Media Foundation]","c74445b2-a2ec-4c77-a8bf-61a6b54cef75","mf.mfgetattributesize","mfapi/MFGetAttributeSize"]
old-location: mf\mfgetattributesize.htm
tech.root: mf
ms.assetid: c74445b2-a2ec-4c77-a8bf-61a6b54cef75
ms.date: 12/05/2018
ms.keywords: MFGetAttributeSize, MFGetAttributeSize function [Media Foundation], c74445b2-a2ec-4c77-a8bf-61a6b54cef75, mf.mfgetattributesize, mfapi/MFGetAttributeSize
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
 - MFGetAttributeSize
 - mfapi/MFGetAttributeSize
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
 - MFGetAttributeSize
---

# MFGetAttributeSize function


## -description

Retrieves an attribute whose value is a size, expressed as a width and height.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

<b>GUID</b> that identifies which value to retrieve. The attribute type must be MF_ATTRIBUTE_UINT64.

### -param punWidth [out]

Receives the width.

### -param punHeight [out]

Receives the height.

## -returns

This function can return one of these values.

## -remarks

Some attributes specify a size as a packed <b>UINT64</b> value. Use this function to get the numerator and denominator as separate 32-bit values.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize">MFSetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>