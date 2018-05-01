---
UID: NF:rometadataapi.IMetaDataImport.EnumEvents
title: IMetaDataImport::EnumEvents method
author: windows-driver-content
description: Enumerates event definition tokens for the specified TypeDef token.
old-location: winrt\imetadataimport_enumevents.htm
old-project: WinRT
ms.assetid: 442b5db1-1e5f-4314-9c53-dbd0f0651d3c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EnumEvents method [Windows Runtime], EnumEvents method [Windows Runtime], IMetaDataImport interface, EnumEvents,IMetaDataImport.EnumEvents, IMetaDataImport, IMetaDataImport interface [Windows Runtime], EnumEvents method, IMetaDataImport::EnumEvents, rometadataapi/IMetaDataImport::EnumEvents, winrt.imetadataimport_enumevents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.EnumEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::EnumEvents method


## -description


Enumerates event definition tokens for the specified TypeDef token.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tkTypDef [in]

The TypeDef token whose event definitions are to be enumerated.




### -param rgEvents [out]

The array of returned events.


### -param cMax [in]

The maximum size of the <i>rgEvents</i> array.


### -param pcEvents [out]

The actual number of events returned in <i>rgEvents</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumEvents</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no events to enumerate. In this case, <i>pcEvents</i> is zero.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

