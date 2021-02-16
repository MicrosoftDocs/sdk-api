---
UID: NF:bits.IEnumBackgroundCopyFiles.GetCount
title: IEnumBackgroundCopyFiles::GetCount (bits.h)
description: Retrieves a count of the number of files in the enumeration.
helpviewer_keywords: ["GetCount","GetCount method [BITS]","GetCount method [BITS]","IEnumBackgroundCopyFiles interface","IEnumBackgroundCopyFiles interface [BITS]","GetCount method","IEnumBackgroundCopyFiles.GetCount","IEnumBackgroundCopyFiles::GetCount","_drz_ienumbackgroundcopyfiles_getcount","bits.ienumbackgroundcopyfiles_getcount","bits/IEnumBackgroundCopyFiles::GetCount"]
old-location: bits\ienumbackgroundcopyfiles_getcount.htm
tech.root: Bits
ms.assetid: 24a9d5f9-e923-4b20-8abf-8ce50fc2602b
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyFiles interface, IEnumBackgroundCopyFiles interface [BITS],GetCount method, IEnumBackgroundCopyFiles.GetCount, IEnumBackgroundCopyFiles::GetCount, _drz_ienumbackgroundcopyfiles_getcount, bits.ienumbackgroundcopyfiles_getcount, bits/IEnumBackgroundCopyFiles::GetCount
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
 - IEnumBackgroundCopyFiles::GetCount
 - bits/IEnumBackgroundCopyFiles::GetCount
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
 - IEnumBackgroundCopyFiles.GetCount
---

# IEnumBackgroundCopyFiles::GetCount


## -description

Retrieves a count of the number of files in the enumeration.

## -parameters

### -param puCount [out]

Number of files in the enumeration.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>