---
UID: NF:imapi2.IDiscFormat2Erase.get_FullErase
title: IDiscFormat2Erase::get_FullErase (imapi2.h)
description: Determines the quality of the disc erasure. (Get)
helpviewer_keywords: ["IDiscFormat2Erase interface [IMAPI]","get_FullErase method","IDiscFormat2Erase.get_FullErase","IDiscFormat2Erase::get_FullErase","get_FullErase","get_FullErase method [IMAPI]","get_FullErase method [IMAPI]","IDiscFormat2Erase interface","imapi.idiscformat2erase_get_fullerase","imapi2/IDiscFormat2Erase::get_FullErase"]
old-location: imapi\idiscformat2erase_get_fullerase.htm
tech.root: imapi
ms.assetid: 56b4db17-1699-4e09-9a6d-ef5e998621c5
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],get_FullErase method, IDiscFormat2Erase.get_FullErase, IDiscFormat2Erase::get_FullErase, get_FullErase, get_FullErase method [IMAPI], get_FullErase method [IMAPI],IDiscFormat2Erase interface, imapi.idiscformat2erase_get_fullerase, imapi2/IDiscFormat2Erase::get_FullErase
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IDiscFormat2Erase::get_FullErase
 - imapi2/IDiscFormat2Erase::get_FullErase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Erase.get_FullErase
---

# IDiscFormat2Erase::get_FullErase


## -description

Determines the quality of the disc erasure.

## -parameters

### -param value [out]

Is VARIANT_TRUE if the erase operation fully erases the disc by overwriting the  entire medium at least once. 

Is VARIANT_FALSE if the erase operation overwrites the  directory tracks, but not the entire disc. This option requires less time to perform than the full erase option.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-erasemedia">IDiscFormat2Erase::EraseMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-put_fullerase">IDiscFormat2Erase::put_FullErase</a>
