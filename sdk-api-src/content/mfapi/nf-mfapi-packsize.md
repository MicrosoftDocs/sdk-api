---
UID: NF:mfapi.PackSize
title: PackSize function (mfapi.h)
description: Packs a UINT32 width value and a UINT32 height value into a UINT64 value that represents a size.
helpviewer_keywords: ["PackSize","PackSize function [Media Foundation]","mf.packsize","mfapi/PackSize"]
old-location: mf\packsize.htm
tech.root: mf
ms.assetid: F3DCEEA5-2D88-49FC-87DB-DEB0AE48E984
ms.date: 12/05/2018
ms.keywords: PackSize, PackSize function [Media Foundation], mf.packsize, mfapi/PackSize
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - PackSize
 - mfapi/PackSize
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
 - PackSize
---

# PackSize function


## -description

Packs a UINT32 width value and a UINT32 height value into a UINT64 value that represents a size.

## -parameters

### -param unWidth [in]

Value to store the <b>UINT32</b> width value.

### -param unHeight [in]

Value to store the <b>UINT32</b> height value.

## -returns

Returns the packed <b>UINT64</b> value.

## -remarks

This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64">IMFAttributes::SetUINT64</a> method.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio">MFGetAttributeRatio</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize">MFGetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>