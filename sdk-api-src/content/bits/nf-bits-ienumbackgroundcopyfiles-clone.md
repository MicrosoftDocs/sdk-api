---
UID: NF:bits.IEnumBackgroundCopyFiles.Clone
title: IEnumBackgroundCopyFiles::Clone (bits.h)
description: Creates another IEnumBackgroundCopyFiles enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [BITS]","Clone method [BITS]","IEnumBackgroundCopyFiles interface","IEnumBackgroundCopyFiles interface [BITS]","Clone method","IEnumBackgroundCopyFiles.Clone","IEnumBackgroundCopyFiles::Clone","_drz_ienumbackgroundcopyfiles_clone","bits.ienumbackgroundcopyfiles_clone","bits/IEnumBackgroundCopyFiles::Clone"]
old-location: bits\ienumbackgroundcopyfiles_clone.htm
tech.root: Bits
ms.assetid: ea2d2f76-7cd9-4e48-8a2c-3dd367afdee7
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyFiles interface, IEnumBackgroundCopyFiles interface [BITS],Clone method, IEnumBackgroundCopyFiles.Clone, IEnumBackgroundCopyFiles::Clone, _drz_ienumbackgroundcopyfiles_clone, bits.ienumbackgroundcopyfiles_clone, bits/IEnumBackgroundCopyFiles::Clone
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumBackgroundCopyFiles::Clone
 - bits/IEnumBackgroundCopyFiles::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyFiles.Clone
---

# IEnumBackgroundCopyFiles::Clone


## -description

Creates another 
<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -parameters

### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnumFiles</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>