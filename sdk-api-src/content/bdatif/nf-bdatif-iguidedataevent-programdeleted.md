---
UID: NF:bdatif.IGuideDataEvent.ProgramDeleted
title: IGuideDataEvent::ProgramDeleted
author: windows-sdk-content
description: The ProgramDeleted method is called when a program has been deleted.
old-location: mstv\iguidedataevent_programdeleted.htm
tech.root: mstv
ms.assetid: 4a71e139-1c09-473c-8195-0a55601d2f17
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ProgramDeleted method, IGuideDataEvent.ProgramDeleted, IGuideDataEvent::ProgramDeleted, IGuideDataEventProgramDeleted, ProgramDeleted, ProgramDeleted method [Microsoft TV Technologies], ProgramDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ProgramDeleted, mstv.iguidedataevent_programdeleted
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
 - IGuideDataEvent.ProgramDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdatif.h
: 
- IGuideDataEvent.ProgramDeleted
: 
---

# IGuideDataEvent::ProgramDeleted


## -description



The <b>ProgramDeleted</b> method is called when a program has been deleted.



Currently the <a href="https://msdn.microsoft.com/en-us/library/Dd693011(v=VS.85).aspx">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.


## -parameters




### -param varProgramDescriptionID [in]

Specifies the unique identifier of the program that was deleted.


## -returns



Return S_OK if successful, or an error code.




## -remarks



The event sink is not required to support this event; it may return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent Interface</a>
 

 

