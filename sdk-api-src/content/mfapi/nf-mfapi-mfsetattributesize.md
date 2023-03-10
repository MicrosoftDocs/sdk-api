---
UID: NF:mfapi.MFSetAttributeSize
title: MFSetAttributeSize function (mfapi.h)
description: Sets width and height as a single 64-bit attribute value.
helpviewer_keywords: ["MFSetAttributeSize","MFSetAttributeSize function [Media Foundation]","cf7b3cfe-fdce-417d-8c0b-198d026b8768","mf.mfsetattributesize","mfapi/MFSetAttributeSize"]
old-location: mf\mfsetattributesize.htm
tech.root: mf
ms.assetid: cf7b3cfe-fdce-417d-8c0b-198d026b8768
ms.date: 12/05/2018
ms.keywords: MFSetAttributeSize, MFSetAttributeSize function [Media Foundation], cf7b3cfe-fdce-417d-8c0b-198d026b8768, mf.mfsetattributesize, mfapi/MFSetAttributeSize
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
 - MFSetAttributeSize
 - mfapi/MFSetAttributeSize
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
 - MFSetAttributeSize
---

# MFSetAttributeSize function


## -description

Sets width and height as a single 64-bit attribute value.

## -parameters

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

A <b>GUID</b> that identifies the value to set. If this key already exists, the function overwrites the old value.

### -param unWidth [in]

The width.

### -param unHeight [in]

The height.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Some attributes specify a width and a height as a packed <b>UINT64</b> value. This function packs the width and height values into a single <b>UINT64</b> value.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize">MFGetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>