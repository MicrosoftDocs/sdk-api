---
UID: NN:imapi2.DDiscFormat2EraseEvents
title: DDiscFormat2EraseEvents
author: windows-sdk-content
description: Implement this interface to receive notifications of the current erase operation.
old-location: imapi\ddiscformat2eraseevents.htm
old-project: imapi
ms.assetid: 0e999859-d409-4fd8-a5da-c43da64bcd8f
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: DDiscFormat2EraseEvents, DDiscFormat2EraseEvents interface [IMAPI], DDiscFormat2EraseEvents interface [IMAPI],described, imapi.ddiscformat2eraseevents, imapi2/DDiscFormat2EraseEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2EraseEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DDiscFormat2EraseEvents interface


## -description


Implement this interface to receive notifications of the current erase operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DDiscFormat2EraseEvents</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>DDiscFormat2EraseEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DDiscFormat2EraseEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current erase operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>
 

 

