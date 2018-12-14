---
UID: NF:pla.IDataCollectorSet.put_SegmentMaxSize
title: IDataCollectorSet::put_SegmentMaxSize
author: windows-sdk-content
description: Retrieves or sets the maximum size of any log file in the data collector set.
old-location: pla\idatacollectorset_get_segmentmaxsize.htm
tech.root: pla
ms.assetid: 7dd96822-a398-42c3-94f1-b9cd7a647575
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorSet interface [PLA],SegmentMaxSize property, IDataCollectorSet.SegmentMaxSize, IDataCollectorSet.put_SegmentMaxSize, IDataCollectorSet::SegmentMaxSize, IDataCollectorSet::get_SegmentMaxSize, IDataCollectorSet::put_SegmentMaxSize, SegmentMaxSize property [PLA], SegmentMaxSize property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_segmentmaxsize, pla.idatacollectorset_get_segmentmaxsize, pla/IDataCollectorSet::SegmentMaxSize, pla/IDataCollectorSet::get_SegmentMaxSize, pla/IDataCollectorSet::put_SegmentMaxSize, put_SegmentMaxSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.SegmentMaxSize
 - IDataCollectorSet.get_SegmentMaxSize
 - IDataCollectorSet.put_SegmentMaxSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::put_SegmentMaxSize


## -description


Retrieves or sets the maximum size of any log file in the data collector set.  

This property is read/write.


## -parameters


## -remarks



When the maximum size is reached, PLA creates a new log file to write to if the <a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a> property is enabled.

PLA tries to limit the log file size to this value; however, the actual size of the log file might grow slightly larger than this value.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a>



<a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">IDataCollectorSet::SegmentMaxDuration</a>
 

 

