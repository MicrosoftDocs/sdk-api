---
UID: NF:bdatif.IGuideDataEvent.GuideDataAcquired
title: IGuideDataEvent::GuideDataAcquired
author: windows-sdk-content
description: The GuideDataAcquired method is called when a complete set of guide data has been acquired from the current transport stream.
old-location: mstv\iguidedataevent_guidedataacquired.htm
tech.root: mstv
ms.assetid: 00f1aec7-4d26-4323-9d7e-c75d9a0c374c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GuideDataAcquired, GuideDataAcquired method [Microsoft TV Technologies], GuideDataAcquired method [Microsoft TV Technologies],IGuideDataEvent interface, IGuideDataEvent interface [Microsoft TV Technologies],GuideDataAcquired method, IGuideDataEvent.GuideDataAcquired, IGuideDataEvent::GuideDataAcquired, IGuideDataEventGuideDataAcquired, bdatif/IGuideDataEvent::GuideDataAcquired, mstv.iguidedataevent_guidedataacquired
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.GuideDataAcquired
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent::GuideDataAcquired


## -description



The <b>GuideDataAcquired</b> method is called when a complete set of guide data has been acquired from the current transport stream.



Currently the <a href="https://msdn.microsoft.com/en-us/library/Dd693011(v=VS.85).aspx">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.


## -parameters






## -returns



Return S_OK if successful, or an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent Interface</a>
 

 

