---
UID: NF:imapi2.IDiscFormat2Data.get_PostgapAlreadyInImage
title: IDiscFormat2Data::get_PostgapAlreadyInImage
author: windows-sdk-content
description: Determines if the data stream contains post-writing gaps.
old-location: imapi\idiscformat2data_get_postgapalreadyinimage.htm
old-project: imapi
ms.assetid: 4f4423b8-8cda-4ef2-a8f6-4ef7e147bf6b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_PostgapAlreadyInImage method, IDiscFormat2Data.get_PostgapAlreadyInImage, IDiscFormat2Data::get_PostgapAlreadyInImage, get_PostgapAlreadyInImage, get_PostgapAlreadyInImage method [IMAPI], get_PostgapAlreadyInImage method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_postgapalreadyinimage, imapi2/IDiscFormat2Data::get_PostgapAlreadyInImage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2Data.get_PostgapAlreadyInImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Data::get_PostgapAlreadyInImage


## -description


Determines if the data stream contains post-writing gaps.


## -parameters




### -param value [out]

Is VARIANT_TRUE if the data stream contains post-writing gaps; otherwise, VARIANT_FALSE. 


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




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/68dba44b-ac14-4473-9b74-917ce2c5054a">IDiscFormat2Data::put_PostgapAlreadyInImage</a>
 

 

