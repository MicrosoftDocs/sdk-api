---
UID: NF:imapi2.IDiscFormat2Data.put_ForceMediaToBeClosed
title: IDiscFormat2Data::put_ForceMediaToBeClosed (imapi2.h)
description: Determines if further additions to the file system are prevented. (Put)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","put_ForceMediaToBeClosed method","IDiscFormat2Data.put_ForceMediaToBeClosed","IDiscFormat2Data::put_ForceMediaToBeClosed","imapi.idiscformat2data_put_forcemediatobeclosed","imapi2/IDiscFormat2Data::put_ForceMediaToBeClosed","put_ForceMediaToBeClosed","put_ForceMediaToBeClosed method [IMAPI]","put_ForceMediaToBeClosed method [IMAPI]","IDiscFormat2Data interface"]
old-location: imapi\idiscformat2data_put_forcemediatobeclosed.htm
tech.root: imapi
ms.assetid: 9a087a73-1b61-481d-8deb-a251511906a9
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],put_ForceMediaToBeClosed method, IDiscFormat2Data.put_ForceMediaToBeClosed, IDiscFormat2Data::put_ForceMediaToBeClosed, imapi.idiscformat2data_put_forcemediatobeclosed, imapi2/IDiscFormat2Data::put_ForceMediaToBeClosed, put_ForceMediaToBeClosed, put_ForceMediaToBeClosed method [IMAPI], put_ForceMediaToBeClosed method [IMAPI],IDiscFormat2Data interface
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
 - IDiscFormat2Data::put_ForceMediaToBeClosed
 - imapi2/IDiscFormat2Data::put_ForceMediaToBeClosed
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
 - IDiscFormat2Data.put_ForceMediaToBeClosed
---

# IDiscFormat2Data::put_ForceMediaToBeClosed


## -description

Determines if further additions to the file system are prevented.

## -parameters

### -param value [in]

Set to VARIANT_TRUE to mark the disc as closed to prohibit additional writes when the next write session ends.

Set to VARIANT_FALSE to keep the disc open for subsequent write sessions. The default is VARIANT_FALSE.

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
<dt><b>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0400

</td>
</tr>
</table>

## -remarks

When the free space on a disc reaches 2% or less, the write process marks the disc closed, regardless of the value of this property. This action ensures that a disc has enough free space to record a file system in a write session.

You can erase a rewritable disc that is marked closed.

Note that the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_disableconsumerdvdcompatibilitymode">IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode</a> property may supersede this property. Please refer to <b>put_DisableConsumerDvdCompatibilityMode</b> for details.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_forcemediatobeclosed">IDiscFormat2Data::get_ForceMediaToBeClosed</a>
