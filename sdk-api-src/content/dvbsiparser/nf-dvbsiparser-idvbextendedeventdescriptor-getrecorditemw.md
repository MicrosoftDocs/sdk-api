---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDvbExtendedEventDescriptor::GetRecordItemW


## -description


Gets the item and descriptor from a  Digital Videl Broadcast (DVB) extended event descriptor, in Unicode string format.


## -parameters




### -param bRecordIndex [in]

Specifies the item record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>
  method to get the number of records in the extended event descriptor.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrDesc [out]

Pointer to a buffer that receives the item description. The caller is responsible for freeing this memory.


### -param pbstrItem [out]

Pointer to a buffer that receives the item text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>



<a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>
 

 

