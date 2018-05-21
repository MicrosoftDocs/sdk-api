---
UID: NF:mpeg2data.IMpeg2TableFilter.RemoveExtension
title: IMpeg2TableFilter::RemoveExtension
author: windows-driver-content
description: The RemoveExtension method removes a table extension from the list of MPEG-2 table sections that the filter sends.
old-location: mstv\impeg2tablefilter_removeextension.htm
old-project: mstv
ms.assetid: 1f29f29d-d411-44b7-bedb-6d10c49a0d4d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMpeg2TableFilter interface [Microsoft TV Technologies],RemoveExtension method, IMpeg2TableFilter.RemoveExtension, IMpeg2TableFilter::RemoveExtension, IMpeg2TableFilterRemoveExtension, RemoveExtension, RemoveExtension method [Microsoft TV Technologies], RemoveExtension method [Microsoft TV Technologies],IMpeg2TableFilter interface, mpeg2data/IMpeg2TableFilter::RemoveExtension, mstv.impeg2tablefilter_removeextension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2data.h
api_name:
-	IMpeg2TableFilter.RemoveExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpeg2TableFilter::RemoveExtension


## -description



The <b>RemoveExtension</b> method removes a table extension from the list of MPEG-2 table sections that the filter sends.




## -parameters




### -param p [in]

Specifies the packet identifier (PID) of the table.


### -param t [in]

Specifies the table identifier (TID) of the table.


### -param e [in]

Specifies the table_extension identifier to remove from the list.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/9467352d-44a5-41eb-b426-28df83a6d423">IMpeg2TableFilter Interface</a>
 

 

