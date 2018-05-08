---
UID: NF:mpeg2data.IMpeg2TableFilter.AddPID
title: IMpeg2TableFilter::AddPID
author: windows-driver-content
description: The AddPID method adds a packet identifier (PID) to the list of PIDs that the filter sends.
old-location: mstv\impeg2tablefilter_addpid.htm
old-project: mstv
ms.assetid: 7a811d1f-cb1b-4f45-8dee-ba83efd20709
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AddPID, AddPID method [Microsoft TV Technologies], AddPID method [Microsoft TV Technologies],IMpeg2TableFilter interface, IMpeg2TableFilter interface [Microsoft TV Technologies],AddPID method, IMpeg2TableFilter.AddPID, IMpeg2TableFilter::AddPID, IMpeg2TableFilterAddPID, mpeg2data/IMpeg2TableFilter::AddPID, mstv.impeg2tablefilter_addpid
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
-	IMpeg2TableFilter.AddPID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpeg2TableFilter::AddPID


## -description



The <b>AddPID</b> method adds a packet identifier (PID) to the list of PIDs that the filter sends.




## -parameters




### -param p [in]

Specifies the PID of the transport stream packets to examine.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/9467352d-44a5-41eb-b426-28df83a6d423">IMpeg2TableFilter Interface</a>
 

 

