---
UID: NF:bits5_0.IBackgroundCopyFile5.SetProperty
title: IBackgroundCopyFile5::SetProperty (bits5_0.h)
description: Sets a generic property of a BITS file transfer.
helpviewer_keywords: ["IBackgroundCopyFile5 interface [BITS]","SetProperty method","IBackgroundCopyFile5.SetProperty","IBackgroundCopyFile5::SetProperty","SetProperty","SetProperty method [BITS]","SetProperty method [BITS]","IBackgroundCopyFile5 interface","bits.ibackgroundcopyfile5_setproperty","bits5_0/IBackgroundCopyFile5::SetProperty"]
old-location: bits\ibackgroundcopyfile5_setproperty.htm
tech.root: Bits
ms.assetid: 7a5809ef-e84f-4566-a5fa-fd63b1dfd15c
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile5 interface [BITS],SetProperty method, IBackgroundCopyFile5.SetProperty, IBackgroundCopyFile5::SetProperty, SetProperty, SetProperty method [BITS], SetProperty method [BITS],IBackgroundCopyFile5 interface, bits.ibackgroundcopyfile5_setproperty, bits5_0/IBackgroundCopyFile5::SetProperty
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
 - IBackgroundCopyFile5::SetProperty
 - bits5_0/IBackgroundCopyFile5::SetProperty
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
 - IBackgroundCopyFile5.SetProperty
---

# IBackgroundCopyFile5::SetProperty


## -description

Sets a generic property of a BITS file transfer.

## -parameters

### -param PropertyId [in]

Specifies the property to be set.

### -param PropertyValue [out]

A pointer to a union that specifies the value to be set. The union member appropriate for the property ID is used.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bits5_0/nn-bits5_0-ibackgroundcopyfile5">IBackgroundCopyFile5</a>



<a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-getproperty">IBackgroundCopyFile5.GetProperty</a>