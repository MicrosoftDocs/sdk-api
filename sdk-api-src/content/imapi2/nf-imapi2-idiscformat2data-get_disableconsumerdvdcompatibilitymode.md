---
UID: NF:imapi2.IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode
title: IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode (imapi2.h)
description: Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD. (Get)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","get_DisableConsumerDvdCompatibilityMode method","IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode","IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode","get_DisableConsumerDvdCompatibilityMode","get_DisableConsumerDvdCompatibilityMode method [IMAPI]","get_DisableConsumerDvdCompatibilityMode method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_get_disableconsumerdvdcompatibilitymode","imapi2/IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode"]
old-location: imapi\idiscformat2data_get_disableconsumerdvdcompatibilitymode.htm
tech.root: imapi
ms.assetid: dc88f657-0ec1-488d-8110-055de06c2d58
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_DisableConsumerDvdCompatibilityMode method, IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode, IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode, get_DisableConsumerDvdCompatibilityMode, get_DisableConsumerDvdCompatibilityMode method [IMAPI], get_DisableConsumerDvdCompatibilityMode method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_disableconsumerdvdcompatibilitymode, imapi2/IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode
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
 - IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode
 - imapi2/IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode
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
 - IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode
---

# IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode


## -description

Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

## -parameters

### -param value [out]

Is VARIANT_TRUE if the session skips the tasks that allow the disc to play on more consumer devices

Is VARIANT_FALSE if the media will be written to maximize read compatibility with consumer devices.

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

## -remarks

This property has no effect on CD media.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_disableconsumerdvdcompatibilitymode">IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode</a>
