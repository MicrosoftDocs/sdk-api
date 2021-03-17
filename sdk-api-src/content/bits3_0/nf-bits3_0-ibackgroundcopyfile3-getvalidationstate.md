---
UID: NF:bits3_0.IBackgroundCopyFile3.GetValidationState
title: IBackgroundCopyFile3::GetValidationState (bits3_0.h)
description: Gets the current validation state of this file.
helpviewer_keywords: ["GetValidationState","GetValidationState method [BITS]","GetValidationState method [BITS]","IBackgroundCopyFile3 interface","IBackgroundCopyFile3 interface [BITS]","GetValidationState method","IBackgroundCopyFile3.GetValidationState","IBackgroundCopyFile3::GetValidationState","bits.ibackgroundcopyfile3_getvalidationstate","bits3_0/IBackgroundCopyFile3::GetValidationState"]
old-location: bits\ibackgroundcopyfile3_getvalidationstate.htm
tech.root: Bits
ms.assetid: 705644e2-fd15-4225-b26a-e75c2dd2f6e3
ms.date: 12/05/2018
ms.keywords: GetValidationState, GetValidationState method [BITS], GetValidationState method [BITS],IBackgroundCopyFile3 interface, IBackgroundCopyFile3 interface [BITS],GetValidationState method, IBackgroundCopyFile3.GetValidationState, IBackgroundCopyFile3::GetValidationState, bits.ibackgroundcopyfile3_getvalidationstate, bits3_0/IBackgroundCopyFile3::GetValidationState
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
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
 - IBackgroundCopyFile3::GetValidationState
 - bits3_0/IBackgroundCopyFile3::GetValidationState
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
 - IBackgroundCopyFile3.GetValidationState
---

# IBackgroundCopyFile3::GetValidationState


## -description

Gets the current validation state of this file.

## -parameters

### -param pState [out]

<b>TRUE</b> if the contents of the file is valid, otherwise, <b>FALSE</b>.

## -returns

The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

Note that <b>FALSE</b> may not mean that the file is not valid, it may mean the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate">IBackgroundCopyFile3::SetValidationState</a> has not been called.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate">IBackgroundCopyFile3::SetValidationState</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacherecord-isfilevalidated">IBitsPeerCacheRecord::IsFileValidated</a>