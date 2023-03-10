---
UID: NF:wcmconfig.IItemEnumerator.MoveNext
title: IItemEnumerator::MoveNext (wcmconfig.h)
description: Moves the current position to the next item in the enumerator if available.
helpviewer_keywords: ["IItemEnumerator interface [SMI]","MoveNext method","IItemEnumerator.MoveNext","IItemEnumerator::MoveNext","MoveNext","MoveNext method [SMI]","MoveNext method [SMI]","IItemEnumerator interface","smi.iitemenumerator_movenext","wcmconfig/IItemEnumerator::MoveNext"]
old-location: smi\iitemenumerator_movenext.htm
tech.root: SMI
ms.assetid: bdec3ee4-e66a-4e93-9109-c5721d06eb63
ms.date: 12/05/2018
ms.keywords: IItemEnumerator interface [SMI],MoveNext method, IItemEnumerator.MoveNext, IItemEnumerator::MoveNext, MoveNext, MoveNext method [SMI], MoveNext method [SMI],IItemEnumerator interface, smi.iitemenumerator_movenext, wcmconfig/IItemEnumerator::MoveNext
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IItemEnumerator::MoveNext
 - wcmconfig/IItemEnumerator::MoveNext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - IItemEnumerator.MoveNext
---

# IItemEnumerator::MoveNext


## -description

Moves the current position to the next item in the enumerator if available.

## -parameters

### -param ItemValid [out]

Returns <b>True</b> if a valid item is found in the position after the move.

## -returns

This method returns an HRESULT value.

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
Indicates success.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This method always returns <b>S_OK</b> on success, regardless of the state of the enumeration. If there are no more items, <i>ItemValid</i> is set to <b>False</b>, and this is how to determine if the end of the enumeration has been reached.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a>