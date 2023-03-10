---
UID: NF:imapi2.IDiscFormat2Data.put_PostgapAlreadyInImage
title: IDiscFormat2Data::put_PostgapAlreadyInImage (imapi2.h)
description: Determines if the data stream contains post-writing gaps. (Put)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","put_PostgapAlreadyInImage method","IDiscFormat2Data.put_PostgapAlreadyInImage","IDiscFormat2Data::put_PostgapAlreadyInImage","imapi.idiscformat2data_put_postgapalreadyinimage","imapi2/IDiscFormat2Data::put_PostgapAlreadyInImage","put_PostgapAlreadyInImage","put_PostgapAlreadyInImage method [IMAPI]","put_PostgapAlreadyInImage method [IMAPI]","IDiscFormat2Data interface"]
old-location: imapi\idiscformat2data_put_postgapalreadyinimage.htm
tech.root: imapi
ms.assetid: 68dba44b-ac14-4473-9b74-917ce2c5054a
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],put_PostgapAlreadyInImage method, IDiscFormat2Data.put_PostgapAlreadyInImage, IDiscFormat2Data::put_PostgapAlreadyInImage, imapi.idiscformat2data_put_postgapalreadyinimage, imapi2/IDiscFormat2Data::put_PostgapAlreadyInImage, put_PostgapAlreadyInImage, put_PostgapAlreadyInImage method [IMAPI], put_PostgapAlreadyInImage method [IMAPI],IDiscFormat2Data interface
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
 - IDiscFormat2Data::put_PostgapAlreadyInImage
 - imapi2/IDiscFormat2Data::put_PostgapAlreadyInImage
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
 - IDiscFormat2Data.put_PostgapAlreadyInImage
---

# IDiscFormat2Data::put_PostgapAlreadyInImage


## -description

Determines if the data stream contains post-writing gaps.

## -parameters

### -param value [in]

Set to VARIANT_TRUE if the data stream contains post-writing gaps; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.

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

Note that writing to CD-R/RW media will automatically append a post-gap of 150 sectors, unless this property is explicitly disabled.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_postgapalreadyinimage">IDiscFormat2Data::get_PostgapAlreadyInImage</a>
