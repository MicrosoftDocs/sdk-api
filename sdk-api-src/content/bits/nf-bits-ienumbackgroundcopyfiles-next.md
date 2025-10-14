---
UID: NF:bits.IEnumBackgroundCopyFiles.Next
title: IEnumBackgroundCopyFiles::Next (bits.h)
description: Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements. (IEnumBackgroundCopyFiles.Next)
helpviewer_keywords: ["IEnumBackgroundCopyFiles interface [BITS]","Next method","IEnumBackgroundCopyFiles.Next","IEnumBackgroundCopyFiles::Next","Next","Next method [BITS]","Next method [BITS]","IEnumBackgroundCopyFiles interface","_drz_ienumbackgroundcopyfiles_next","bits.ienumbackgroundcopyfiles_next","bits/IEnumBackgroundCopyFiles::Next"]
old-location: bits\ienumbackgroundcopyfiles_next.htm
tech.root: Bits
ms.assetid: ac62533a-8949-41b9-a3e6-f9030884a9ce
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyFiles interface [BITS],Next method, IEnumBackgroundCopyFiles.Next, IEnumBackgroundCopyFiles::Next, Next, Next method [BITS], Next method [BITS],IEnumBackgroundCopyFiles interface, _drz_ienumbackgroundcopyfiles_next, bits.ienumbackgroundcopyfiles_next, bits/IEnumBackgroundCopyFiles::Next
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
 - IEnumBackgroundCopyFiles::Next
 - bits/IEnumBackgroundCopyFiles::Next
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
 - IEnumBackgroundCopyFiles.Next
---

# IEnumBackgroundCopyFiles::Next


## -description

Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> objects. You must release each object in <i>rgelt</i> when done.

### -param pceltFetched [out]

Number of elements returned in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one. Otherwise, initialize the value of <i>pceltFetched</i> to 0 before calling this method.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Successfully returned the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned less than the number of requested elements.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>
