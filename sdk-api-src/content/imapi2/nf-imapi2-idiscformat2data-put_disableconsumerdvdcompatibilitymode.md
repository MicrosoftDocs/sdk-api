---
UID: NF:imapi2.IDiscFormat2Data.put_DisableConsumerDvdCompatibilityMode
title: IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode (imapi2.h)
description: Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD. (Put)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","put_DisableConsumerDvdCompatibilityMode method","IDiscFormat2Data.put_DisableConsumerDvdCompatibilityMode","IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode","imapi.idiscformat2data_put_disableconsumerdvdcompatibilitymode","imapi2/IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode","put_DisableConsumerDvdCompatibilityMode","put_DisableConsumerDvdCompatibilityMode method [IMAPI]","put_DisableConsumerDvdCompatibilityMode method [IMAPI]","IDiscFormat2Data interface"]
old-location: imapi\idiscformat2data_put_disableconsumerdvdcompatibilitymode.htm
tech.root: imapi
ms.assetid: d32bbb33-0cb6-46cd-8a06-7ddd6e94a7b3
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],put_DisableConsumerDvdCompatibilityMode method, IDiscFormat2Data.put_DisableConsumerDvdCompatibilityMode, IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode, imapi.idiscformat2data_put_disableconsumerdvdcompatibilitymode, imapi2/IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode, put_DisableConsumerDvdCompatibilityMode, put_DisableConsumerDvdCompatibilityMode method [IMAPI], put_DisableConsumerDvdCompatibilityMode method [IMAPI],IDiscFormat2Data interface
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
 - IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode
 - imapi2/IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode
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
 - IDiscFormat2Data.put_DisableConsumerDvdCompatibilityMode
---

# IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode


## -description

Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

## -parameters

### -param value [in]

Set to VARIANT_TRUE to skip the tasks that allow the disc to play on more consumer devices. Removing compatibility reduces the  recording session time and the need for less free space on disc.

Set to VARIANT_FALSE to increase the chance that a device can play the DVD. The default is VARIANT_FALSE.

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

This property has no effect on CD media and DVD dash media.

For DVD+R and DVD+DL media, this property will also affect the media closing operation. 

<table>
<tr>
<th>Value of DisableConsumerDvdCompatibilityMode </th>
<th>Value of ForceMediaToBeClosed </th>
<th>Closure operation</th>
</tr>
<tr>
<td>False</td>
<td>True</td>
<td>Closes the disc in compatible mode</td>
</tr>
<tr>
<td>False</td>
<td>False</td>
<td>Closes the disc in compatible mode</td>
</tr>
<tr>
<td>True</td>
<td>True</td>
<td>Closes the disc normally</td>
</tr>
<tr>
<td>True</td>
<td>False</td>
<td>Closes the session for DVD+R Closes disc normally for DVD+R DL 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_disableconsumerdvdcompatibilitymode">IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode</a>
