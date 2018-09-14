---
UID: NF:imapi2.IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode
title: IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode
author: windows-sdk-content
description: Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.
old-location: imapi\idiscformat2data_get_disableconsumerdvdcompatibilitymode.htm
tech.root: imapi
ms.assetid: dc88f657-0ec1-488d-8110-055de06c2d58
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_DisableConsumerDvdCompatibilityMode method, IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode, IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode, get_DisableConsumerDvdCompatibilityMode, get_DisableConsumerDvdCompatibilityMode method [IMAPI], get_DisableConsumerDvdCompatibilityMode method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_disableconsumerdvdcompatibilitymode, imapi2/IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.get_DisableConsumerDvdCompatibilityMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This property has no affect on CD media.




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/d32bbb33-0cb6-46cd-8a06-7ddd6e94a7b3">IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode</a>
 

 

