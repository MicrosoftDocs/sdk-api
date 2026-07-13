---
UID: NF:bits5_0.IBackgroundCopyFile5.GetProperty
title: IBackgroundCopyFile5::GetProperty (bits5_0.h)
description: Gets a generic property of a BITS file transfer.
helpviewer_keywords: ["GetProperty","GetProperty method [BITS]","GetProperty method [BITS]","IBackgroundCopyFile5 interface","IBackgroundCopyFile5 interface [BITS]","GetProperty method","IBackgroundCopyFile5.GetProperty","IBackgroundCopyFile5::GetProperty","bits.ibackgroundcopyfile5_getproperty","bits5_0/IBackgroundCopyFile5::GetProperty"]
old-location: bits\ibackgroundcopyfile5_getproperty.htm
tech.root: Bits
ms.assetid: 7afe4d11-f611-40ea-be94-7825f95576de
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [BITS], GetProperty method [BITS],IBackgroundCopyFile5 interface, IBackgroundCopyFile5 interface [BITS],GetProperty method, IBackgroundCopyFile5.GetProperty, IBackgroundCopyFile5::GetProperty, bits.ibackgroundcopyfile5_getproperty, bits5_0/IBackgroundCopyFile5::GetProperty
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile5::GetProperty
 - bits5_0/IBackgroundCopyFile5::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile5.GetProperty
---

# IBackgroundCopyFile5::GetProperty


## -description

Gets a generic property of a BITS file transfer.

## -parameters

### -param PropertyId [in]

Specifies the file property whose value is to be retrieved.

### -param PropertyValue [out]

The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union. Use the union field appropriate for the property ID value passed in.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bits5_0/nn-bits5_0-ibackgroundcopyfile5">IBackgroundCopyFile5</a>



<a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-setproperty">IBackgroundCopyFile5.SetProperty</a>